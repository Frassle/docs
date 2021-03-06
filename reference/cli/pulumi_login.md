## pulumi login

Log into the Pulumi Cloud

### Synopsis


Log into the Pulumi Cloud.  You can script by using PULUMI_ACCESS_TOKEN environment variable.

```
pulumi login [flags]
```

### Options

```
  -c, --cloud-url string   A cloud URL to log into
  -h, --help               help for login
```

### Options inherited from parent commands

```
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output (default true)
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
      --profiling string             Emit CPU and memory profiles and an execution trace to '[filename].[pid].{cpu,mem,trace}', respectively
      --tracing string               Emit tracing to a Zipkin-compatible tracing endpoint
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

### SEE ALSO
* [pulumi](pulumi.md)	 - 

###### Auto generated by spf13/cobra on 14-Jun-2018
