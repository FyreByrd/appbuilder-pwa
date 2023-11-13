# appbuilder-pwa

A template for building a Progressive Web App with [Scripture App Builder](https://softare.sil.org/scriptureappbuilder).

## Prerequisites

-   Visual Studio Code
-   Node 16.17.0+ (we recommend using [Volta](https://volta.sh) to manage the Node versions)

## Usage

You will need to download [Scripture App Builder 10.3.2](https://software.sil.org/scriptureappbuilder/download/) to use this project without the provided example data.

### Develop

Install dependencies with `npm install`.

The PWA depends on data files generated by Scripture App Builder. There is example data provided in the repo. To convert the base data files and run the PWA, do one of the following:

#### Example Data

-   Run `npm run convert:examples` to use the data in the `example_data` folder.
-   Run `npm run dev:noconvert` to start the development server.

#### Scripture App Builder Project

-   Run `Build PWA Data Files` in Scripture App Builder to generate the the base data files from a project
-   Run `npm run dev` to convert the base data files to a format needed for the PWA and run the development server. Changes to the base database files are watched and applied to the running PWA.

> Contact [chris_hubbard@sil.org](mailto:chris_hubbard@sil.org) for the feature key to enable `Build PWA Data Files`

> Note: The book conversion step can take up to several minutes depending on the amount of scripture in the project and the speed of your computer's hard drive.

### Build

Run `npm run build` to build an app with the data provided by `Build PWA Data Files`.

Run `npm run build:examples` to build an app with the example data.

The production build can be viewed by running `npm run preview`.
The production build can be deployed to a public webserver for testing using [Surge](https://surge.sh).

### Testing

Scripture App Builder PWA uses [Vitest](https://vitest.dev/guide/) for unit tests. See that added test files and tests adhere to the [Front End Testing Style Guide](https://github.com/nikeshghimire77/unit-testing-styleguide).

```bash
├── scripts
│   ├── scripture-reference-utils.test.ts
│   └── scripture-reference-utils.ts
```

Run `npm test` to run created test files.

### Deployment

This project is configured by default with the static adaptor, which will allow deployment on any platform that requires a static site.
