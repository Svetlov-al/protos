# Contributing

## Workflow

1. Create a branch from `main`.
2. Make changes.
3. Regenerate Go code if `.proto` files changed.
4. Open a pull request with a clear description.

## Code generation

Run:

```sh
protoc -I proto proto/sso/sso.proto \
  --go_out=./gen/go --go_opt=paths=source_relative \
  --go-grpc_out=./gen/go --go-grpc_opt=paths=source_relative
```
