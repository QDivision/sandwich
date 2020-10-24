# `sandwich`

This repo is the entrypoint for the sandwich local setup. The files in this repo allow developers to quickly and easily stand up the all sandwich services, databases, and UIs on their local machines.

## Getting Started

> Make sure you have all the [prerequisites](#prerequisites) installed before running these commands.

```
git clone git@github.com:QDivision/sandwich.git
cd sandwich
chip sync
chip install
chip start
chip logs
```

## Prerequisites

Install the following tools if you do not already have them:

> **NOTE:** If you use `fish`, install `sdkman` and `nvm` using `bash` because Chip will run stuff in `bash`.

- [Docker for Mac](https://docs.docker.com/docker-for-mac/install/)
- [`brew`](https://brew.sh/):
  ```
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  ```
- [`maven`](https://maven.apache.org/):
  ```
  brew install maven
  ```
- [`yarn`](https://yarnpkg.com/lang/en/):
  ```
  brew install yarn
  ```
- [`sdkman`](https://sdkman.io/):
  ```
  curl -s "https://get.sdkman.io" | bash
  # or
  curl -s "https://get.sdkman.io" | zsh
  ```
- [`nvm`](https://github.com/nvm-sh/nvm):
  ```
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash
  # or
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | zsh
  ```
- [`chip`](https://github.com/QDivision/chip):
  ```
  yarn global add @qdivision/chip
  ```

## Services

These repos contain all the code for the sandwich services and UI:

- https://github.com/QDivision/sandwich-ui
- https://github.com/QDivision/emoji-api
- https://github.com/QDivision/ingredient-api
- https://github.com/QDivision/sandwich-api

## DB Queries

You can query the sandwich DBs using `pgcli` with the following commands:

```
# sandwich-api database:
PGPASSWORD=admin pgcli --user admin --host localhost --dbname sandwichdb --port 5000

# ingredient-api database:
PGPASSWORD=admin pgcli --user admin --host localhost --dbname fooddb --port 5001

# emoji-api database:
PGPASSWORD=admin pgcli --user admin --host localhost --dbname emojidb --port 5002
```

## RabbitMQ Dashboard

You can view the RabbitMQ management dashboard at http://localhost:15002. Login using the following credentials:

```
Username: admin
Password: admin
```
