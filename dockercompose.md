Docker Compose:
===============

Docker Compose is a tool used to define and run multi-container Docker applications.
It allows you to configure multiple containers (example: application + database + cache) using a single file called docker-compose.yml and start them together using one command.


Example of Docker Compose File:
==============================

docker-compose.yml

version: "3.8"

services:
  app:
    build: .
    ports:
      - "3000:3000"
    depends_on:
      - db

  db:
    image: mysql:8
    environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: testdb
    ports:
      - "3306:3306"


Commands:
==========

Start containers:

---
docker compose up -d
---

Stop and remove containers:

---
docker compose down
---