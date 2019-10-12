<h1 align="center"> SCSS Spinners and Loaders </h1>

<p align="center">
    <a href="hthttps://forthebadge.com">
        <img alt="Uses-CSS" src="https://forthebadge.com/images/badges/uses-css.svg">
    </a>&nbsp;&nbsp;&nbsp;
    <a href="https://forthebadge.com">
        <img alt="Built-With-Love" src="https://forthebadge.com/images/badges/built-with-love.svg" />
    </a>
</p>

<p align="center">
    <a href="https://www.npmjs.com/package/scss-spinners">
        <img alt="NPM" src="https://nodei.co/npm/scss-spinners.png?compact=true">
    </a>
</p>

<p align="center">
    <a href="https://circleci.com/gh/RinMinase/anidb">
        <img alt="Circle-CI" src="https://img.shields.io/circleci/project/github/RinMinase/anidb/master.svg?logo=circleci">
    </a>
    <a href="https://www.npmjs.com/package/semantic-release">
        <img alt="Semantic-Release" src="https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg">
    </a>
</p>

## Introduction

## Demo
You can view the spinners right now at [https://rinminase.github.io/scss-spinners/](https://rinminase.github.io/scss-spinners)

## Getting Started

### Using this project as SCSS
1. Install the package from [npm](https://www.npmjs.com/package/scss-spinners)

    ```
    npm install scss-spinners
    ```

2. Import the main stylesheet of this project to the main stylesheet of your project

    ```css
    @import "~scss-spinners/spinners";
    ```

3. Usage is as simple as

    ```html
    <div class="spinner round"></div>
    ```

### Specific imports (Tree-shaking)

To import only a specific spinner:

```scss
@import "~scss-spinners/components/balls";
```

The example above would only import `balls` spinner.

### Overriding variables

Variables is located at `/node_modules/scss-spinners/variables.scss`.

The table below lists the possible variables which can be overriden.

| Task               | Description                                         |
| ------------------ | --------------------------------------------------- |
| `$spinner-color`   | Sets the primary color of the spinner               |
| `$spinner-accent`  | Sets the secondary or accent color of the spinner   |
| `$spinner-size`    | Sets the size of the spinner                        |

To override, on the stylesheet before importing `spinners.scss`:

```scss
$spinner-color: blue;
$spinner-size: 10px;

@import "~scss-spinners/spinners";
```

### Building the project as CSS
1. [Download](https://nodejs.org/en/) the latest Node version. This is marked as `<version number> Current`. Install it on your machine.

2. _(Optional)_ [Download](https://yarnpkg.com/latest.msi) Yarn. This is a faster package manager than the default `npm` one.

3. Clone the project

    ```
    git clone https://github.com/RinMinase/scss-spinners.git
    cd scss-spinners
    ```

4. Install the dependencies then run the project

    ```
    npm install
    npm build
    ```

    **Note:** If you have installed Yarn, run these instead:

    ```
    yarn install
    yarn build
    ```

5. Navigate to the `dist/` folder in the root directory. Inside this folder is your css file for usage.

### Project Structure
    .
    ├── spinners.scss         # Main stylesheet
    ├── globals.scss          # Globals stylesheet
    ├── index.html            # Demo page
    ├── .circleci/            # CircleCI deployment
    ├── components/           # Specific spinner stylesheets
    └── dist/                 # Stylesheets built to CSS

#### How the structure works?
- `spinner.scss` imports all specific spinner stylesheets
- `_{spinner}.scss` imports `variables.scss`, `globals.scss` and contains styles for the specific spinner

### Project tasks

Task automation is based on [Yarn scripts](https://yarnpkg.com/lang/en/docs/cli/run/) or [NPM scripts](https://docs.npmjs.com/misc/scripts).

| Task                             | Description                                                     |
| -------------------------------- | --------------------------------------------------------------- |
| `npm start` or `yarn start`      | Builds the scss files to `dist/` to a css file                  |
| `npm build` or `yarn build`      | Builds the scss files to `dist/` to a minified css file         |
| `npm run watch` or `yarn watch`  | Builds the scss files to `dist/` with file watching on changes  |

## Built with
* <img width=20 height=20 src="https://sass-lang.com/favicon.ico"> [Sassy CSS (SCSS)](https://sass-lang.com/) - CSS pre-processor
* <img width=20 height=20 src="https://nodejs.org/static/images/favicons/favicon-32x32.png"> [NodeJS](https://nodejs.org/) - Environment
* <img width=20 height=20 src="https://dmmj3mmt94rvw.cloudfront.net/favicon-undefined.ico"> [Circle CI](https://circleci.com/) - Continuous Integration (CI) service

## Credits
This is based from [Webkul's CSSPIN](https://github.com/webkul/csspin) made in SCSS for projects looking for SCSS spinners or loaders.
