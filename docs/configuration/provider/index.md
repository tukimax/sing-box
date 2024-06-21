# OutboundProvider

### Structure

```json
{
  "outbound_providers": [
    {
      "type": "",
      "tag": "",
      "path": "",
      "enable_healthcheck": false,
      "healthcheck_url": "https://www.gstatic.com/generate_204",
      "healthcheck_interval": "1m",
      "healthcheck_when_network_change": false,
      "override_dialer": {},

      ... // Filter Fields
    }
  ]
}
```

### Fields

| Type     | Format             |
|----------|--------------------|
| `remote` | [Remote](./remote) |
| `local`  | [Local](./local)   |

#### tag

The tag of the outbound provider.

#### path

==Required==

The path of the outbound provider file.

#### enable_healthcheck

Health check outbounds in outbound provider or not.

Health check will always happen in init status.

#### healthcheck_url

The url for health check of the outbound provider.

Default is `https://www.gstatic.com/generate_204`.

#### healthcheck_interval

The interval for health check of the outbound provider. `1m` will be used if empty.

#### override_dialer

Override dialer fields of outbounds in provider, see [Override Dialer](/configuration/outbound_providers/override_dialer/) for details.

### Filter Fields

See [Filter Fields](/configuration/shared/filter/) for details.
