# ExAmpleData

Makes it easy to generate example data for your app. Can be useful in dev for seed data, in test for test data and sometimes in production for sales/demo data.

Goals:
- Easy. I include a single dependency, Faker, because generating quality example data is hard and it does a good job.
- Valid. Use changesets to help make sure that generated/seed data is validated before being inserted.
- Efficient. Don't hide building associations. When each factory builds its own relationships, its far too easy to build too many, slowing things (especially tests) down.

It's really easy to build the exact object graph you want:

```
account = create(:account)
contact = create(:contact, account_id: account.id)
invoice = create(:invoice, contact_id: contact.id)
```

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `ex_ample_data` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:ex_ample_data, "~> 0.1.0"}
  ]
end
```

## Usage

** TODO **

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at [https://hexdocs.pm/ex_ample_data](https://hexdocs.pm/ex_ample_data).
