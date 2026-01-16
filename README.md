# Protos

Protocol Buffer definitions and generated Go code for SSO.

## Structure

- `proto/` - source `.proto` files
- `gen/go/` - generated Go code

## Requirements

- `protoc`
- `protoc-gen-go`
- `protoc-gen-go-grpc`

## Generate Go code

```sh
protoc -I proto proto/sso/sso.proto \
  --go_out=./gen/go --go_opt=paths=source_relative \
  --go-grpc_out=./gen/go --go-grpc_opt=paths=source_relative
```
