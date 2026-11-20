# Changelog

## [1.2.2] - 2026-11-20

- fix: `deploy/rollback.sh front` sans version précisée échouait (« $4: unbound variable ») car ssh perdait l'argument vide

## [1.2.1] - 2026-11-20

- fix: construire le front sous Node 26 dans `deploy/deploy.sh` (foncier_front 1.3.0) et y installer Yarn 1, que l'image node:26 ne fournit plus

## [1.2.0] - 2026-10-02

- feat: deploy Foncier to the personal VPS preprod (`deploy/deploy.sh`, `deploy/rollback.sh`, `docker-compose.preprod.yml`)
- feat: initialise the preprod database with the real schema and fictitious data (`deploy/db/init-db.sh`)
- feat: stub the EPA SI API in preprod (`/__si-stub/v1/zacs`, `/__si-stub/v1/lots`)
- feat: expose the preprod Postgres on the VPS localhost for DBeaver (127.0.0.1:5433, through an SSH tunnel)
- feat: follow foncier_back 1.2.1, `bien.d_demolition` is a DATE in the schema and the seed
- feat: restore a production dump into the local database (`deploy/db/restore-prod-dump.sh`)

## [1.1.0] - 2026-01-13

- chore: upgrade the container to php:8.4-fpm
