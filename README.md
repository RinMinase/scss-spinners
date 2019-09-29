<h1 align="center"> SCSS Spinners and Loaders </h1>

## Introduction

## Demo
You can view the spinners right now at [https://rinminase.github.io/scss-spinners/](https://rinminase.github.io/scss-spinners)

## Getting Started

### Using this project as SCSS
1. Install the package from `npm`

    ```
    npm install scss-spinners
    ```

2. Import the main stylesheet of this project to the main stylesheet of your project

    ```css
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
    └── components/           # Specific spinner stylesheets

#### How the structure works?
- `spinner.scss` imports `globals.scss` and all specific spinner stylesheets
- `_{spinner}.scss` imports `globals.scss` and contains styles for the specific spinner

### Project tasks

Task automation is based on [Yarn scripts](https://yarnpkg.com/lang/en/docs/cli/run/) or [NPM scripts](https://docs.npmjs.com/misc/scripts).

| Task                             | Description                                                     |
| -------------------------------- | --------------------------------------------------------------- |
| `npm start` or `yarn start`      | Builds the scss files to `dist/` to a css file                  |
| `npm build` or `yarn build`      | Builds the scss files to `dist/` to a minified css file         |
| `npm run watch` or `yarn watch`  | Builds the scss files to `dist/` with file watching on changes  |

## Credits
This is based from [Webkul's CSSPIN](https://github.com/webkul/csspin) made in SCSS for projects looking for SCSS spinners or loaders.