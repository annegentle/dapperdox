# DapperDox

Beautiful, integrated, OpenAPI documentation.

> Themed documentation generator, server and API explorer for OpenAPI (Swagger) Specifications. Helps you build integrated, browsable reference documentation and guides. For example, the [Companies House Developer Hub](https://developer.companieshouse.gov.uk/api/docs/) built with the alpha version.

## Project Status

DapperDox works fine.

You can download the latest DapperDox release from [releases](https://github.com/DapperDox/dapperdox/releases).

## Usage

Detailed usage instructions are available on the comprehensive [website](http://dapperdox.io).

## Features

* Author full documentation in GitHub Flavoured Markdown.
* Document multiple API specifications as a suite of cross-referenced products.
* Seamlessly overlay content onto the automatically generated reference documentation.
* Integrate the built-in API explorer with your APIs and authentication model.
* Proxy your developer platform, allowing full integration of API key management.
* Choose from multiple themes, or create your own.


## Quickstart

First build DapperDox (this assumes that you have your golang environment configured correctly):
```bash
go get && go build
```

Then start up DapperDox, pointing it to your OpenAPI 2.0 specification file:

```
./dapperdox -spec-dir=<location of OpenAPI 2.0 spec>
```

DapperDox looks for the file path `spec/swagger.json` at the `-spec-dir` location, and builds reference documentation for the OpenAPI specification it finds. For example, the obligatory *petstore* OpenAPI specification is provided in the `examples/specifications/petstore` directory, so
passing parameter `-spec-dir=examples/specifications/petstore` will build the petstore documentation.

DapperDox will default to serving documentation from port 3123 on all interfaces, so you can point your 
web browser at http://127.0.0.1:3123 or http://localhost:3123.

For an out-of-the-box example, execute the example run script:

```bash
./run_example.sh
```

This demonstrates many of the configuration options available. See [configuration](http://dapperdox.io/docs/configuration-guide).

## Acknowledgements

Many thanks to [Ian Kent](https://github.com/ian-kent) who began the Golang implementation of DapperDox
as part of a bigger project, from nothing more than a rough spec and by trying to figure out how the Perl
alpha version worked! His commit history was lost when DapperDox was extracted into a stand-alone project, but
its core retains his original and valuable work.

[David Mort](https://github.com/davidmort) for painstaking testing, and bug fixing.





