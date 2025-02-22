---
type: docs
title: "rad application connections CLI reference"
linkTitle: "rad application connections"
slug: rad_application_connections
url: /reference/cli/rad_application_connections/
description: "Details on the rad application connections Radius CLI command"
---
## rad application connections

Shows the connections for an application.

### Synopsis

Shows the connections for an application

```
rad application connections [flags]
```

### Examples

```

# Show connections for current application
rad app connections

# Show connections for specified application
rad app connections my-application
```

### Options

```
  -a, --application string   The application name
  -e, --environment string   The environment name
  -g, --group string         The resource group name
  -h, --help                 help for connections
  -w, --workspace string     The workspace name
```

### Options inherited from parent commands

```
      --config string   config file (default "$HOME/.rad/config.yaml")
  -o, --output string   output format (supported formats are json, table) (default "table")
```

### SEE ALSO

* [rad application]({{< ref rad_application.md >}})	 - Manage Radius Applications

