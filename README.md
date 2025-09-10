# Quote Editor (Hotrails.dev Tutorial)

This is a learning project following the [Hotrails.dev](https://www.hotrails.dev) tutorial. It demonstrates a modern Ruby on Rails 8 application using Hotwire (Turbo + Stimulus), PostgreSQL, and a modern asset pipeline.

## Features

- Add, edit, and delete quotes
- Real-time updates with Hotwire (Turbo Streams)
- Modern Rails 8 conventions
- Stimulus controllers for interactivity
- System and model tests

## Project Structure

- `app/models/quote.rb` — Quote model with validations and Turbo Streams broadcasting
- `app/controllers/quotes_controller.rb` — CRUD actions for quotes
- `app/views/quotes/` — Views and Turbo Stream templates for quotes
- `app/javascript/` — JavaScript entrypoint and Stimulus controllers
- `app/assets/stylesheets/` — SCSS stylesheets, organized by components/layouts/mixins
- `db/migrate/` — Database migrations (e.g., create_quotes)
- `test/` — System, model, and controller tests
- `config/routes.rb` — RESTful routes for quotes
- `Procfile.dev` — For running Rails, JS, and CSS in development

## Tech Stack

- Ruby on Rails 8
- PostgreSQL
- Hotwire (Turbo, Stimulus)
- SCSS (Sass)
- esbuild & sass for asset bundling

## Setup Instructions

1. **Install dependencies:**
   - Ruby (see `.ruby-version` if present)
   - PostgreSQL
   - Node.js & npm
2. **Install gems:**
   ```sh
   bundle install
   ```
3. **Install JS dependencies:**
   ```sh
   npm install
   ```
4. **Set up the database:**
   ```sh
   bin/rails db:setup
   ```
5. **Run the app (development):**
   ```sh
   bin/dev
   ```
   Or, manually:
   ```sh
   bin/rails server
   npm run build -- --watch
   npm run build:css -- --watch
   ```

## Running Tests

```sh
bin/rails test
bin/rails test:system
```

## Learning Resources

- [Hotrails.dev](https://www.hotrails.dev) — The tutorial this project is based on
- [Hotwire.dev](https://hotwired.dev) — Hotwire documentation
- [Rails Guides](https://guides.rubyonrails.org/)

---

This project is for educational purposes and follows the Hotrails.dev step-by-step approach to building a modern Rails app with Hotwire.
