# My favorite 4 P.R. links

- [Postgres & register A.P.I.](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/8)
- [Register usage](https://github.com/classroom-angel/labs11_prop_mngmt-FE/pull/8)
- [Lots of models](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/17)
- [Lots of reorganization](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/18)

## Individual Accomplishments this Sprint

This first sprint has went very well. We started off slow with all of the planning, but it seems like it's already pretty close to paying off. I've operated in the same way with the code itself. I've been trying to organize everything that I've been making so that it's scalable and still sensible. With what we have so far, there's a good chance a lot of our file structure could be used for something pretty clever.

## Detailed Analysis

For the [Postgres & register A.P.I. P.R.](https://github.com/classroom-angel/labs11_prop_mngmt-BE/pull/8), I set up postgresql to work locally and on heroku. I also implemented the register route for user creation while I was at it. As for postgres, I tried to get it working locally following [this guide](https://github.com/Lambda-School-Labs/Labs8-OfflineReader/wiki/Setting-up-a-PostgreSQL-database-for-local-testing). My recommendation is to replace pgAdmin4 with something else (i.e., [TablePlus](https://tableplus.io/)).
As for what else is needed to get postgresql configured:
- have this in .env, replacing the capitalized fields with your values:
`DATABASE_URL=postgres://USER:PASS@localhost:5432/DB_NAME`.
- add this config for development and production in your knexfile:
```javascript
{
  client: 'pg',
  connection: process.env.DATABASE_URL,
  migrations: {
    directory: __dirname + '/db/migrations'
  },
  seeds: {
    directory: __dirname + '/db/seeds'
  }
}
```

## Milestone Reflections

I wrote nearly the whole schema (with a bit of help here and there), which definitely helped me get my head around how the data would all work, or at least how it _could_ work. We ended up passing through our T.D.D. inspection the first go round, getting everything deployed, completing our user model, and seeding 500 users. I think we pretty much hit everything out of the park.
