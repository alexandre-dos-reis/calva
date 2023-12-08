# Config Specification

## Examples

```toml
title = "Api tests"

[vars]
foo = "bar"
link = "https://my-api.com"

[baz]
method = "get"
url = "{{ link }}"

[bar]
methods = ["get", "post"]
url = "https://my-api.com"
headers = {
  Authorization = "Bearer some-api-key",
  OtherHeader = "{{ .env.secret-key }}"
}

# Todos
[servers]

[servers.alpha]
ip = "10.0.0.1"
role = "frontend"

[servers.beta]
ip = "10.0.0.2"
role = "backend"
```
