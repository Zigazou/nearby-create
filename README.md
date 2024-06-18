# Nearby-Create

Welcome to Nearby-Create! This project aims to provide a script for users to
generate an SQLite3 database targetted at discovering public transport
facilities nearby geographic coordinates in France.

It actually works for the Métropole Rouen Normandie region but can be adapted
to suit any french region.

In order to do so, it uses `transport.data.gouv.fr`, a french government
website pointing to open data.

## Getting Started

To get started with Nearby-Create, follow these steps:

1. Clone the repository: `git clone https://github.com/Zigazou/nearby-create.git`
2. Navigate to the project directory: `cd nearby-create`
3. Create the database: `python3 nearby-create-database.py transport.db`

Note: if the database already exists, it will delete and recreate it!

## Features

- The script queries the `transport.data.gouv.fr` site to find files to
  download.
- Names are corrected to allow a better user experience.
- A three character prefix is added to each identifier thus allowing having
  multiplce sources in the same tables.
- Data not needed for finding transport facilities are wiped from the database.

The database structure is given by the `nearby-create-database.db.dia`.

## Requirements

- Python 3
- Requests
