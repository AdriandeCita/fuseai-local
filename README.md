# FuseAI local setup

This is a Docker Compose setup for running [FuseAI project](https://github.com/bitswired/fuseai). This setup is made for purely local/personal use, and it may not support multi-user setup.

## Why

- "Setup once and forget", especially helpful if you're not fluent in docker.
- Database is stored on host system, and does not depend on persistence of the container itself.

## HowTo

- Clone this repository
- Prepare local environment variables:
  - You can use `.env.example` file for it, just copy it into `.env` and fill in your data inside.
  - Or you can set them manually through command line when running docker-compose:

      ```sh
      export JWT_KEY="secret" && export ADMIN_EMAIL="admin@admin.com" && export ADMIN_PASSWORD="password" ...
      ```

- Run docker-compose:

  ```sh
  docker-compose up
  ```

  ...or if you prefer to set environment variable through command-line:

  ```sh
  export JWT_KEY="secret" && export ADMIN_EMAIL="admin@admin.com" && export ADMIN_PASSWORD="password" && docker-compose up
  ```

- Visit [http://localhost:3030/](http://localhost:3030/).
- Log in using the credentials you've set in the variables above.
- Add you OpenAI API key in settings.
- Start chatting!

Please refer to [original documentation](https://github.com/bitswired/fuseai#%EF%B8%8F-how-to-run) if you want more options or have issues running the project.
