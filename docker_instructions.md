# Docker environment

Every topic can run in a throwaway container so my laptop stays clean.

```bash
# Python, SQL, general
docker run --rm -it -v "$PWD":/work -w /work python:3.12 bash

# Go
docker run --rm -it -v "$PWD":/work -w /work golang:1.24 bash

# Terraform
docker run --rm -it -v "$PWD":/work -w /work hashicorp/terraform:1.10 -help

# Postgres for sql-learn
docker run --rm -d --name pg -e POSTGRES_PASSWORD=learn -p 5432:5432 postgres:16
```
