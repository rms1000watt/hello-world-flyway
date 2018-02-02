# Hello World Flyway

## Introduction

Hello World to FlywayDB

## Contents

- [Installation](#installation)
- [Usage](#usage)
- [Naming Convention](#naming-convention)

## Installation

Install `Docker for Mac` manually

Then run:

```bash
# Install FlywayDB
brew install flyway
```

## Usage

```bash
# Start Postgres
docker-compose up -d

# Run migration
flyway migrate

# Look at your Database

# Then undo migration (requires paid version)
flyway undo
```

## Naming Convention

- `V` at the beginning stands for `Version` which is used for Migrations
- `U` at the beginning stands for `Undo` which is used for Undos

- `V1` stands for `Version 1` of the database
- `V1_1` stands for `Step 1` for `Version 1` of the database
- `V1_2` stands for `Step 2` for `Version 1` of the database
- `V2` stands for `Version 2` of the database
- `V2_1` stands for `Step 1` for `Version 2` of the database
- `V2_2` stands for `Step 2` for `Version 2` of the database

- Similarly for `U`

- Every `V` should have a coresponding `U` so you can move forward and backward through the database version (Think: Finite State Machine!!!)
