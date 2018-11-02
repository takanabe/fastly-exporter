# fastly-exporter [![Latest Release](https://img.shields.io/github/release/peterbourgon/fastly-exporter.svg?style=flat-square)](https://github.com/peterbourgon/fastly-exporter/releases/latest) [![Travis CI](https://travis-ci.org/peterbourgon/fastly-exporter.svg?branch=master)](https://travis-ci.org/peterbourgon/fastly-exporter)

This program consumes from the [Fastly Real-time Analytics API][rt] and makes
the data available to [Prometheus][prom].

[rt]: https://docs.fastly.com/api/analytics
[prom]: https://prometheus.io

## Getting

Go to the [releases page](/releases), or, if you have a working Go installation,
you can install the latest revision from HEAD.

```
go get github.com/peterbourgon/fastly-exporter
```

## Using

```
USAGE
  fastly-exporter [flags]

FLAGS
  -debug false                             Log debug information
  -endpoint http://127.0.0.1:8080/metrics  Prometheus /metrics endpoint
  -namespace ...                           Prometheus namespace (optional)
  -service ...                             Specific Fastly service ID (optional, repeatable)
  -subsystem ...                           Prometheus subsystem (optional)
  -token ...                               Fastly API token (required)

VERSION
  2.0.0
```

A valid Fastly API -token is mandatory. [See this link][token] for information
on creating API tokens. Providing individual -service IDs is optional, and will
Service IDs are available at the top of your [Fastly dashboard][db]. 

[token]: https://docs.fastly.com/guides/account-management-and-security/using-api-tokens#creating-api-tokens
[db]: https://manage.fastly.com/services/all
