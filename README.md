# Hello Contexts

Code examples and a demonstration apps built in Phoenix 1.3 while reading about contexts in the [Phoenix Guides](https://hexdocs.pm/phoenix/overview.html). This is part of larger effort found [here](https://github.com/smeade/hellophoenix).

- [ ] **Contexts**
  - [x] Overview [
    [guide](https://hexdocs.pm/phoenix/contexts.html)
    ]
  - [x] Adding an Accounts Context With Generators [
    [guide](https://hexdocs.pm/phoenix/contexts.html#adding-an-accounts-context) |
    [code:controller](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/controllers/user_controller.ex) |    [code:context](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/accounts.ex) |
    [code:schema](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/user.ex)
    ]
  - [x] In-context Relationships: e.g. has_one, belongs_to [
    [guide](https://hexdocs.pm/phoenix/contexts.html#in-context-relationships) |
    ]
  - [ ] Adding Account Functions: e.g. Sessions [
    [guide](https://hexdocs.pm/phoenix/contexts.html#adding-account-functions)
    ]
  - [ ] Cross-context dependencies: e.g. CMS [
    [guide](https://hexdocs.pm/phoenix/contexts.html#cross-context-dependencies)
    ]
  - [ ] Cross-context data: e.g.  [
    [guide](https://hexdocs.pm/phoenix/contexts.html#cross-context-data)
    ]
  - [ ] Adding CMS functions: e.g. page views [
    [guide](https://hexdocs.pm/phoenix/contexts.html#adding-cms-functions)
    ]


## To start your Phoenix server:

  * Install dependencies with `mix deps.get`
  * Create and migrate your database with `mix ecto.create && mix ecto.migrate`
  * Install Node.js dependencies with `cd assets && npm install`
  * Start Phoenix endpoint with `mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](http://www.phoenixframework.org/docs/deployment).

## Learn more

  * Official website: http://www.phoenixframework.org/
  * Guides: http://phoenixframework.org/docs/overview
  * Docs: https://hexdocs.pm/phoenix
  * Mailing list: http://groups.google.com/group/phoenix-talk
  * Source: https://github.com/phoenixframework/phoenix
