# Saas VS less-css

This repository is devoted to Saas and less css-preprocessors comparison with simple examples explaining why less or sass rocks or fails. Feel free to contribute.

## Examples

Examples are listed here. For each example, the winner is cited.

* `imports-with-overrides`: sequentially import variable definitions and overrides them -- Sass wins.

## Contributing

Do not hesitate to fork this repository and submit real-world examples via a pull request. Your example should respect this example tree:

    example/
    ├── README.md
    ├── less
    │   ├── partial.less
    │   └── styles.less
    └── sass
        ├── _partials.scss
        └── styles.scss

Examples must be pre-processable via:

    $ lessc less/styles.less
    $ scss sass/styles.scss

Do not forget that your example folder should contain a README.md explaining the underling challenge and who's the winner!
