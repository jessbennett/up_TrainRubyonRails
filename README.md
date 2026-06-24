# up_TrainRubyonRails

A Rails application scaffold generated for the up_TrainRubyonRails project.

**Prerequisites**

- Ruby 3.3.0 (see `.ruby-version`)
- Rails 8.1.3
- PostgreSQL 12+ (server running locally or reachable remotely)
- Node (for JavaScript tooling) and a JS package manager (npm/yarn) if you use frontend tooling

**Quick setup (development)**

Run these commands from the project root:

```bash
# install Ruby (rbenv/asdf) and select the version in .ruby-version
# install gem dependencies
bundle install

# copy example env and set values
cp .env.example .env

# create and migrate the database
rails db:create
rails db:migrate
rails db:seed

# start the app (use `bin/dev` if using foreman/overmind)
bin/dev
```

Notes:
- `config/database.yml` is configured for PostgreSQL and will respect `DATABASE_URL` if provided.
- If you prefer to set individual PG variables, use `PG_HOST`, `PG_PORT`, `PG_USERNAME`, `PG_PASSWORD`, and `PG_DATABASE` in your environment.

**Environment example**

See `.env.example` for an example `DATABASE_URL` and other environment variables.

**Running tests**

```bash
rails test
```

**Continuous integration**

This repository includes a starter GitHub Actions workflow at `.github/workflows/ci.yml` to run tests and linters.

**Deployment**

- Set `DATABASE_URL` in your production environment (or configure your provider's database add-on).
- Ensure `RAILS_ENV=production` and compile assets before starting the server.

If you want, I can also:

- update `config/database.yml` to read more env vars by default
- add a `.ruby-version` (already present) or `.ruby-gemset` for rvm users
- create initial migrations and seeds for your domain models

File references:

- `config/database.yml` — database configuration
- `.ruby-version` — Ruby version to use
- `.env.example` — example environment variables
