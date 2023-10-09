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
