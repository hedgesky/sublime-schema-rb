# schema.rb navigation for Sublime Text

This package introduces quick navigation across tables defined in `schema.rb` (Rails-specific file).

## Usage

Just use `Goto Symbol` when you have `schema.rb` opened: <kbd>⌘</kbd><kbd>R</kbd> on Mac, <kbd>Ctrl</kbd><kbd>R</kbd> on Windows.

<img src="https://raw.githubusercontent.com/hedgesky/sublime-schema-rb/master/demo.gif">

## Installation

The easiest way to install is using [Package Control](https://packagecontrol.io/), search for `schema-rb`:

1. Open Command Palette (<kbd>⌘</kbd><kbd>⇧</kbd><kbd>P</kbd> on Mac, <kbd>Ctrl</kbd><kbd>Shift ⇧</kbd><kbd>P</kbd> on Windows)
2. Choose `Package Control: Install Package`
3. Select `schema-rb`

## Integration with ApplySyntax

By default, [ApplySyntax](https://packagecontrol.io/packages/ApplySyntax) disrupts functionality of this package by overriding `schema-rb` syntax with `Ruby on Rails` syntax. To fix that, you could configure ApplySyntax accordingly:

- Open up its settings (`Sublime Text -> Preferences -> Package Settings -> ApplySyntax -> Settings`)
- Add following snippet under `syntaxes` key:

```json
{
    "syntax": "schema-rb/schema-rb.sublime-syntax",
    "rules": [
        {"file_path": ".*/schema.rb$"}
    ]
}
```
