# Check TOML

This linter is for validating TOML configuration files using [MegaLinter](https://github.com/oxsecurity/megalinter) as a plugin.

This linter plugin is a combination of two linters `check-toml` from [pre-commit-hooks](https://github.com/pre-commit/pre-commit-hooks?tab=readme-ov-file#check-toml) and [toml-validator](https://github.com/staticdev/toml-validator).

## Usage

In the `.mega-linter.yml` of your project add the following lines.

``` yaml
PLUGINS:
  - https://raw.githubusercontent.com/hype8912/check-toml-megalinter-plugin/main/mega-linter-plugin-checktoml/checktoml.megalinter-descriptor.yml
```

## Configuration

You can disable the linter plugin by two ways

1. Completely remove or comment out the line from the `.mega-linter.yml` file.

2. Set the TOML checks to disabled in the `.mega-linter.yml` file or in the actions file. Refer to the MegaLinter [Activation and deactivation](https://github.com/oxsecurity/megalinter/blob/main/docs/config-activation.md) for more information.

``` yaml
DISABLE: TOML
```

You can disable the individual linters in the `.mega-linter.yml` file or in the actions file. Refer to the MegaLinter [Activation and deactivation](https://github.com/oxsecurity/megalinter/blob/main/docs/config-activation.md) for more information.

``` yaml
DISABLE_LINTERS: check-toml,toml-validator
```
