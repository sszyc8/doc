---
title: Install using Portainer
description: Step-by-step installation guide
published: 1
date: 2024-07-29T07:05:05.611Z
tags: guide, setup
editor: markdown
dateCreated: 2024-07-29T07:00:46.009Z
---

> This guide was contributed by the community and may be incomplete or become outdated.
{.is-warning}

This guide details the step-by-step procedure to install Wiki.js on a machine running **Portainer**.

1. Click on **Stacks** in the left sidebar navigation.
1. Click on the **+ Add stack** button.
1. Enter a name for the stack (e.g. `wiki`).
1. Select **Web editor** as the Build method.
1. In the Web editor below, paste the following block of code:
    ```yaml
    version: '2'
    services:
      db:
        image: postgres:15-alpine
        environment:
          POSTGRES_DB: wiki
          POSTGRES_PASSWORD: wikijsrocks
          POSTGRES_USER: wikijs
        logging:
          driver: "none"
        restart: unless-stopped
        volumes:
          - db-data:/var/lib/postgresql/data

      wiki:
        image: requarks/wiki:2
        depends_on:
          - db
        environment:
          DB_TYPE: postgres
          DB_HOST: db
          DB_PORT: 5432
          DB_USER: wikijs
          DB_PASS: wikijsrocks
          DB_NAME: wiki
        restart: unless-stopped
        ports:
          - "80:3000"

    volumes:
      db-data:
    ```
1. Click on **Deploy the stack** button.
1. There's no step 7, it was that easy.

You can now navigate to the IP / domain of your server to complete the configuration and start using Wiki.js!
