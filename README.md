# render

![tests](https://github.com/go-chi/render/actions/workflows/test.yml/badge.svg)
[![Go Report Card](https://goreportcard.com/badge/github.com/go-chi/render)](https://goreportcard.com/report/github.com/go-chi/render)
[![Go Reference](https://pkg.go.dev/badge/github.com/go-chi/render.svg)](https://pkg.go.dev/github.com/go-chi/render)

## This is a fork from
* go-chi/render & cinience/render
* With custom json marshaller support from https://github.com/josearomeroj/render/commit/df236ff1849d274f0dc9bb3dd99a961413dab0ea

The `render` package helps manage HTTP request / response payloads.

Every well-designed, robust and maintainable Web Service / REST API also needs
well-*defined* request and response payloads. Together with the endpoint handlers,
the request and response payloads make up the contract between your server and the
clients calling on it.

Typically, in a REST API application, you will have your data models (objects/structs)
that hold lower-level runtime application state, and at times you need to assemble,
decorate, hide or transform the representation before responding to a client. That
server output (response payload) structure, is also likely the input structure to
another handler on the server.

This is where `render` comes in - offering a few simple helpers and interfaces to
provide a simple pattern for managing payload encoding and decoding.

We've also combined it with some helpers for responding to content types and parsing
request bodies. Please have a look at the [rest](https://github.com/go-chi/chi/blob/master/_examples/rest/main.go)
example which uses the latest chi/render sub-pkg.

All feedback is welcome, thank you!
