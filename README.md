# Email Relay Providers Domains

This repository contains a list of domains used from various email relay providers such as SimpleLogin, AnonAddy, and others.
These domains are used to forward emails while protecting the user's real email address.

## Purpose

The purpose of this repository is to identify email addresses originating from email relay services.

## Data Structure

Each item in the list is a JSON object with the following structure:

```json
{
    "name": "string",
    "homepage": "string",
    "pricing": "string (enum)",
    "domains": [
        {
            "domain": "string",
            "pricing": "string (enum)",
            "mxRecords": [
                {
                    "priority": "integer",
                    "hostname": "string"
                }
            ]
        }
    ]
}
```

### Fields

| Field                        | Type                                            | Description                                                                                     |
|------------------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------|
| `name`                       | `string`                                        | The name of the email relay provider.                                                           |
| `homepage`                   | `string`                                        | The homepage URL of the email relay provider.                                                   |
| `pricing`                    | `"FREE" \| "FREEMIUM \| "PREMIUM" \| "UNKNOWN"` | Indicates whether the service is free or paid.                                                  |
| `domains`                    | `array`                                         | An array of objects containing information about thge domains used by the email relay provider. |
| `domains.domain`             | `string`                                        | The domain name used by the email relay provider.                                               |
| `domains.pricing`            | `"FREE" \| "FREEMIUM \| "PREMIUM" \| "UNKNOWN"` | Indicates whether the domain is free or paid.                                                   |
| `domains.mxRecords`          | `array`                                         | An array of objects containing information about the MX records used by the meail provider.     |
| `domains.mxRecords.priority` | `integer`                                       | The priority of the MX record.                                                                  |
| `domains.mxRecords.hostname` | `string`                                        | The hostname of the MX record.                                                                  |

## Contributions

Contributions are welcome! If you know of any additional email relay providers or domains, please feel free to submit a pull request or open an issue.

## Disclaimer

While every effort is made to keep this list up-to-date and accurate, the landscape of email relay providers is constantly changing. Therefore, the information provided here should be used as a guide and not taken as definitive.

## License

This repository is licensed under the [MIT License](LICENSE).