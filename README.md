# Install pkl GitHub Action

This GitHub Action installs [pkl](https://github.com/apple/pkl), a new Apple configuration-as-code language, on Linux or Mac runners.

## Features

- Installs pkl on MacOS and Ubuntu
- Easy to use in your GitHub Actions workflows
- Needed if using pkl code generation in your workflow

## Usage

To use this action in your workflow, add the following step:

```yaml
steps:
  - uses: deezapps-fam/install-pkl@v1
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
      - uses: deezapps-fam/install-pkl@v1
      - name: Run pkl command
        run: | 
          pkl --version
```

## Inputs

This action does not require any inputs.
However, the `version` to download can be optionally specified:

```yaml
steps:
  - uses: deezapps-fam/install-pkl@v1
    with:
      version: '0.25.3'
```

The current default version is `0.25.3`.

## Outputs

This action does not produce any outputs.

## License

This action is licensed under the MIT license.
