# Mix Format
A Github Action to format your Elixir code and commit any changed files to the pull request automagically.

## Inputs:
- `elixir_version` - required. Example: "1.15"
- `otp_version` - required. Example: "26"
- `mix_env` - optional. Defaults to "test".
- `author` - optional. Defaults to github.actor

## Example Usage:
```
name: Make sure Elixir code is formatted 

on:
  pull_request:
    types: [opened, reopened, synchronize]

jobs:
  format:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/mix-format@v1
      with:
        elixir_version: "1.15"
        otp_version: "26"
        mix_env: "dev"
```