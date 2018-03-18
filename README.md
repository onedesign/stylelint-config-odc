# stylelint-config-odc

> The One Design Company shareable config for stylelint.

Use it as is or as a foundation for your own config.

## Installation

```bash
npm install stylelint-config-odc --save-dev
```

## Usage

If you've installed `stylelint-config-odc` locally within your project, just set your `stylelint` config to:

```json
{
  "extends": "stylelint-config-odc"
}
```

If you've globally installed `stylelint-config-odc` using the `-g` flag, then you'll need to use the absolute path to `stylelint-config-odc` in your config e.g.

```json
{
  "extends": "/absolute/path/to/stylelint-config-odc"
}
```

### Extending the config

Simply add a `"rules"` key to your config, then add your overrides and additions there.

For example, to change the `at-rule-no-unknown` rule to use its `ignoreAtRules` option, turn off the `block-no-empty` rule, and add the `unit-whitelist` rule:

```json
{
  "extends": "stylelint-config-odc",
  "rules": {
    "at-rule-no-unknown": [ true, {
      "ignoreAtRules": [
        "extends"
      ]
    }],
    "block-no-empty": null,
    "unit-whitelist": ["em", "rem", "s"]
  }
}
```

