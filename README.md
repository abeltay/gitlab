# Gitlab docker-compose files
## Setup
1. `cp gitlab-example.env gitlab.env`
1. Replace the secrets in `gitlab.env` with randomised keys

Postgres requires the `pg_trgm` module to be enabled in order to work. Run the following commands to enable it in the database
1. `docker-compose up -d postgres`
1. Enter the container
  1. `docker-compose exec postgres sh`
  1. `psql -U gitlab -d gitlabhq_production`
  1. `CREATE EXTENSION pg_trgm;`
1. Exit the container
1. `docker-compose down`

## Maintenance
1. Go to the Gitlab docker-compose folder
1. `git pull origin master`
1. `docker-compose pull`
1. `docker-compose up -d`
