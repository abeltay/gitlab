# Gitlab docker-compose files
## Setup
1. Make necessary configurations in `gitlab.rb`
1. `docker-compose up -d gitlab`
1. `docker cp gitlab.rb <container name>:/etc/gitlab/gitlab.rb`
1. `docker-compose up -d --force-recreate`

Register the runner

## Maintenance
1. Go to the Gitlab docker-compose folder
1. `git pull`
1. `docker-compose pull`
1. `docker-compose up -d`
