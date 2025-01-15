# Lucy x VSCode

I Really Want to Stay At Your House

## Comaand

General comand :

- *Clear Command Palette History*  
    macOS   ` Cmd + Shift + P `  
    windous ` Ctrl + Shift + P `

## Configuration

Preferences that can be inserted in the `settings.json` file:

- `Flake8(E501)`

    ```json
    "flake8.args": [ "--max-line-length=80", ]
    ```

- Module not found `wx`

  ```json
    "pylint.args": [
        "--extension-pkg-whitelist=wx"
    ]
    ```
