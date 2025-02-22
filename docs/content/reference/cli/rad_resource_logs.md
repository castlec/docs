---
type: docs
title: "rad resource logs CLI reference"
linkTitle: "rad resource logs"
slug: rad_resource_logs
url: /reference/cli/rad_resource_logs/
description: "Details on the rad resource logs Radius CLI command"
---
## rad resource logs

Read logs from a running containers resource

### Synopsis

Reads logs from a running resource. Currently only supports the resource type 'Applications.Core/containers'.
This command allows you to access logs of a deployed application and output those logs to the local console.

'rad resource logs' will output all currently available logs for the resource and then exit.

'rad resource logs' will output logs from the resource's primary container. In scenarios like Dapr where multiple containers are in use, the '--container \<name\>' option can specify the desired container.

Specify the '--follow' option to stream additional logs as they are emitted by the resource. When following, press CTRL+C to exit the command and terminate the stream.

```
rad resource logs [resource] [flags]
```

### Examples

```
# read logs from the 'webapp' resource of the current default app
rad resource logs containers webapp

# read logs from the 'orders' resource of the 'icecream-store' application
rad resource logs containers orders --application icecream-store

# stream logs from the 'orders' resource of the 'icecream-store' application
rad resource logs containers orders --application icecream-store --follow

# read logs from the 'daprd' sidecar container of the 'orders' resource of the 'icecream-store' application
rad resource logs containers orders --application icecream-store --container daprd
```

### Options

```
      --container string   specify the container from which logs should be streamed
  -f, --follow             specify that logs should be stream until the command is canceled
  -g, --group string       The resource group name
  -h, --help               help for logs
      --replica string     specify the replica to collect logs from
```

### Options inherited from parent commands

```
  -a, --application string   The application name
      --config string        config file (default "$HOME/.rad/config.yaml")
  -o, --output string        output format (supported formats are json, table) (default "table")
  -w, --workspace string     The workspace name
```

### SEE ALSO

* [rad resource]({{< ref rad_resource.md >}})	 - Manage resources

