---
title: push
description: Pushes a package (.nupkg, .zip, .tar.gz, etc.) package to the built-in NuGet repository in an Octopus Server.
position: 280
---

Pushes a [package](/docs/packaging-applications/create-packages/index.md) (.nupkg, .zip, .tar.gz, etc.) package to the built-in NuGet repository in an Octopus Server.

Learn more about the [built-in repository](/docs/packaging-applications/package-repositories/built-in-repository/index.md).

**push options**

```text
Usage: octo push [<options>]

Where [<options>] is any of:

Package pushing:

      --package=VALUE        Package file to push. Specify multiple packages
                             by specifying this argument multiple times:
                             --package package1 --package package2
      --overwrite-mode=VALUE If the package already exists in the repository,
                             the default behavior is to reject the new
                             package being pushed (FailIfExists). You can use
                             the overwrite mode to OverwriteExisting or
                             IgnoreIfExists.
      --replace-existing     If the package already exists in the repository,
                             the default behavior is to reject the new
                             package being pushed. You can pass this flag to
                             overwrite the existing package. This flag may be
                             deprecated in a future version; passing it is
                             the same as using the OverwriteExisting
                             overwrite-mode.
      --use-delta-compression=VALUE
                             Allows disabling of delta compression when
                             uploading packages to the Octopus Server. (True
                             or False. Defaults to true.)

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

