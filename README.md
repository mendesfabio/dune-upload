# Dune Upload

Programmatically uploads CSV files into Dune database via API.

## Usage

```yaml
name: Dune Upload

on:
  push:
    branches: main

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Dune Upload
      - uses: mendesfabio/dune-upload@v0.0.1
        with:
          dune_api_key: ${{secrets.DUNE_API_KEY}}
          csv_file_path: "example.csv"
          table_name: "example_table"
          description: "example_description"
```
