# Install pkl GitHub Action

This GitHub Action installs [pkl](https://github.com/apple/pkl), a new Apple configuration-as-code language, on Linux runners.

## Features

- Installs pkl on Ubuntu (amd64 and aarch64)
- Easy to use in your GitHub Actions workflows
- Needed if using pkl code generation in your workflow

## Usage

To use this action in your workflow, add the following step:

```yaml
steps:
  - uses: deezapps-fam/install-pkl-action@v1
```

## Example Workflow

Here's an example workflow that uses this action:

```yaml
name: Install pkl
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: deezapps-fam/install-pkl-action@v1
      - name: Run pkl command
        run: | 
          pkl --version
```

## Inputs

This action does not require any inputs.

## Outputs

This action does not produce any outputs.

## License

This action is licensed under the MIT license.
