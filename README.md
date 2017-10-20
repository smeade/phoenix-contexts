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
  - [x] In-context Relationships: e.g. belongs_to, has_one
    - [x] Overview [
      [guide](https://hexdocs.pm/phoenix/contexts.html#in-context-relationships)
      ]
    - [x] mix phx.gen.context Accounts Credential...[
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/credential.ex)
      ]
    - [x] has_one/belongs_to [
      [code:belongs_to](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/credential.ex#L9) | [code:has_one](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/user.ex#L10)
      ]
    - [x] load association data [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/accounts.ex#L43)
      ]
    - [x] add association changeset [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/accounts.ex#L61)
      ]
    - [x] add association to user edit/create form [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/templates/user/form.html.eex#L20-L26)
      ]
    - [x] add association to user show [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/templates/user/show.html.eex#L15-L19)
      ]
  - [x] Adding Account Functions: e.g. Sessions
    - [x] Overview [
      [guide](https://hexdocs.pm/phoenix/contexts.html#adding-account-functions)
      ]
    - [x] Add authenticate_by_email_password function to accounts [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/accounts.ex#L12-L22)
      ]
    - [x] Create session controller [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/accounts/accounts.ex#L12) |
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/controllers/session_controller.ex#L11)
      ]
    - [x] Add sessions to router [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/router.ex#L21-L22)
      ]
    - [x] Add an authentication plug to the router [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/router.ex#L30-L40)
      ]
    - [x] Create session view and template [
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/views/session_view.ex) |
      [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/templates/session/new.html.eex)
      ]
  - [x] Cross-context dependencies: e.g. CMS [
    [guide](https://hexdocs.pm/phoenix/contexts.html#cross-context-dependencies)
    ]
    - New CMS context
      - [x] CMS context
      - [x] Add to router
      - [x] Generate an Author schema
      - [x] Add an author_id field to the pages table
  - [x] Cross-context data: e.g.  [
    [guide](https://hexdocs.pm/phoenix/contexts.html#cross-context-data)
    ]
    - [x] Tie pages to authors and author to users
      - [x] page belongs_to author [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/cms/page.ex#L10)]
      - [x] author has_many pages [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/cms/author.ex#L11)]
      - [x] author belongs_to user [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/cms/author.ex#L12)]
    - [x] Require an author on pages
      - [x] preload data on fetch [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/cms/cms.ex#L14)]
      - [x] persist author data [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/cms/cms.ex#L44)]
      - [x] functions to ensure author exists [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello/cms/cms.ex#L48-L58)]
      - [x] add plug to CMS.PageController [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/controllers/cms/page_controller.ex#L7) | [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/controllers/cms/page_controller.ex#L61-L64)]
      - [x] make use of the values in the connection assigns [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/controllers/cms/page_controller.ex#L21)]
      - [x] display author when showing a page [[code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/templates/cms/page/show.html.eex#L20-L23) | [code](https://github.com/smeade/phoenix-contexts/blob/master/lib/hello_web/views/cms/page_view.ex#L6-L8)]
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
