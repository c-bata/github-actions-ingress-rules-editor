# github-action-ingress-rules-editor

Edit kubernetes ingress rules and apply it.
This action is useful to build feature environments automatically on Github Actions.

## Scenario

![architecture](./architecture.jpg)

This tool to help editing ingress rules in following architecture.

## Command line tool

```
$ ./ingress_rules_editor --help
Usage:
  ./ingress_rules_editor add -ingress=<INGRESS_NAME> -host=<INGRESS_HOST> -service=<SERVICE_NAME> -port=<SERVICE_PORT>
  ./ingress_rules_editor remove -ingress=<INGRESS_NAME> -host=<INGRESS_HOST>

  -host string
        ingress host (required).
  -ingress string
        name of kubernetes ingress (required).
  -namespace string
        kubernetes namespace (optional).
  -path string
        matching path rules of an incoming request (optional). (default "/*")
  -port int
        port number (required when running 'add'). (default -1)
  -service string
        name of kubernetes service (required when running 'add').
```

## LICENSE

This software is licensed under the MIT license, see [LICENSE](./LICENSE) for more information.