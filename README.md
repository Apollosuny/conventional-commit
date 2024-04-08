# Conventional commit

## Basic Usage

- This repo is the demo how we can setup commitlint and husky to format commit when push code to Github.

- Some step to setup:
    
    1. Install dependencies
    ```bash
    npm install -D @commitlint/config-conventional @commitlint/cli husky
    ```
    2. Init husky
    - You should init git before init husky
    - To init husky
    ```bash
    npx husky init
    ```
    - After init, you will see pre-commit file in `.husky`

    3. Create some file for configuration
    - Create file `commit-msg` in folder `.husky`. This helps add commit message linting to commit-msg hook.
    - To config via file, you can create a file `commitlint.config.js` in the root dir.
    ```js
    // add some configuration
    module.export = {
        extends: ['@commitlint/config-conventional']
    }
    ```

    4. Write commit to test it

## References
| Package             | Url                                                                |
| ----------------- | ------------------------------------------------------------------ |
| Husky | https://typicode.github.io/husky |
| Commitlint | https://commitlint.js.org/guides/getting-started.html |
