# ElixirGrpc

**TODO: Add description**

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `elixir_grpc` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:elixir_grpc, "~> 0.1.0"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/elixir_grpc](https://hexdocs.pm/elixir_grpc).

```
grpcurl -plaintext -proto elixir_grpc.proto -d '{"first_name": "Bob", "last_name": "Smith", "age": 40}' localhost:50051 elixir_grpc.User.Create

  {
  "id": 1,
  "firstName": "Bob",
  "lastName": "Smith",
  "age": 40
}
```

```
grpcurl -plaintext -proto elixir_grpc.proto -d '{"id": 1}' localhost:50051 elixir_grpc.User.Get

  {
  "firstName": "Bob",
  "lastName": "Smith",
  "age": 40
}
```

```
grpcurl -plaintext -proto elixir_grpc.proto -d '{"id": 2}' localhost:50051 elixir_grpc.User.Get
ERROR:
Code: NotFound
Message: Some requested entity (e.g., file or directory) was not found

```

