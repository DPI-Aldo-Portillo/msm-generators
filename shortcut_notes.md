# Generating MSM with Shortcuts

## Create Tables
```bash
$ rails generate model movie title:string description

invoke  active_record
create    db/migrate/20231009154718_create_movies.rb
create    app/models/movie.rb
```

## Save Tables

```bash
$ rails db:migrate

== 20231009154718 CreateMovies: migrating =====================================
-- create_table(:movies)
   -> 0.0030s
== 20231009154718 CreateMovies: migrated (0.0031s) ============================

Annotated (1): app/models/movie.rb
```

## Opposite of Migrate

```bash
$ rails db:rollback

== 20231009154718 CreateMovies: reverting =====================================
-- drop_table(:movies)
   -> 0.0023s
== 20231009154718 CreateMovies: reverted (0.0155s) ============================

Model files unchanged.
```

## Better Approach

```bash
$ rails generate draft:resource movie title:string description

identical  app/controllers/movies_controller.rb
invoke  active_record
remove    db/migrate/20231009154718_create_movies.rb
create    db/migrate/20231009155853_create_movies.rb
force    app/models/movie.rb
create  app/views/movies
create  app/views/movies/index.html.erb
create  app/views/movies/show.html.erb
route  RESTful routes
insert  config/routes.rb
```
