---
title: clean-workerpool
description: Cleans all Offline Workers from a WorkerPool
position: 20
---

[Octo.exe](/docs/octopus-rest-api/octo.exe-command-line/index.md) can be used to cleans all offline workers from a worker pool.

Learn about [worker pools](/docs/infrastructure/workers/worker-pools.md).

**clean-workerpool options**

```text
Usage: octo clean-workerpool [<options>]

Where [<options>] is any of:

WorkerPool Cleanup:

      --workerpool=VALUE     Name of a worker pool to clean up.
      --health-status=VALUE  Health status of Workers to clean up (Healthy,
                             Unavailable, Unknown, HasWarnings, Unhealthy).
                             Can be specified many times.
      --disabled=VALUE       [Optional] Disabled status filter of Worker to
                             clean up.
      --calamari-outdated=VALUE
                             [Optional] State of Calamari to clean up. By
                             default ignores Calamari state.
      --tentacle-outdated=VALUE
                             [Optional] State of Tentacle version to clean u-
                             p. By default ignores Tentacle state

Common options:

      --help                 [Optional] Print help for a command
      --helpOutputFormat=VALUE
                             [Optional] Output format for help, only valid
                             option is json
      --outputFormat=VALUE   [Optional] Output format, only valid option is
                             json
      --server=VALUE         [Optional] The base URL for your Octopus Server,
                             e.g., 'https://octopus.example.com/'. This URL
                             can also be set in the OCTOPUS_CLI_SERVER
                             environment variable.
      --apiKey=VALUE         [Optional] Your API key. Get this from the user
                             profile page. Your must provide an apiKey or
                             username and password. If the guest account is
                             enabled, a key of API-GUEST can be used. This
                             key can also be set in the OCTOPUS_CLI_API_KEY
                             environment variable.
      --user=VALUE           [Optional] Username to use when authenticating
                             with the server. Your must provide an apiKey or
                             username and password. This Username can also be
                             set in the OCTOPUS_CLI_USERNAME environment
                             variable.
      --pass=VALUE           [Optional] Password to use when authenticating
                             with the server. This Password can also be set
                             in the OCTOPUS_CLI_PASSWORD environment variable.
      --configFile=VALUE     [Optional] Text file of default values, with one
                             'key = value' per line.
      --debug                [Optional] Enable debug logging
      --ignoreSslErrors      [Optional] Set this flag if your Octopus Server
                             uses HTTPS but the certificate is not trusted on
                             this machine. Any certificate errors will be
                             ignored. WARNING: this option may create a
                             security vulnerability.
      --enableServiceMessages
                             [Optional] Enable TeamCity or Team Foundation
                             Build service messages when logging.
      --timeout=VALUE        [Optional] Timeout in seconds for network
                             operations. Default is 600.
      --proxy=VALUE          [Optional] The URL of the proxy to use, e.g.,
                             'https://proxy.example.com'.
      --proxyUser=VALUE      [Optional] The username for the proxy.
      --proxyPass=VALUE      [Optional] The password for the proxy. If both
                             the username and password are omitted and
                             proxyAddress is specified, the default
                             credentials are used.
      --space=VALUE          [Optional] The name or ID of a space within
                             which this command will be executed. The default
                             space will be used if it is omitted.
      --keepalive=VALUE      [Optional] How frequently (in seconds) to send a
                             TCP keepalive packet.
      --logLevel=VALUE       [Optional] The log level. Valid options are
                             verbose, debug, information, warning, error and
                             fatal. Defaults to 'debug'.
```

