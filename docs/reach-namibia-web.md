# REACH NAMIBIA WEB APPLICATION

### Contents:
- [Pre-requisites](#pre-requisites)
- [Getting started](#getting-started)
- [Configurations](#configuration)
- [Running the application](#run-app)
- [Build and deployment](#build-deploy)

## Pre-requisites <a name="pre-requisites"></a>

This application was developed with [React](https://reactjs.org/) using the [DHIS2 Application Platform](https://platform.dhis2.nu/). The source code was written using [Typescript](https://www.typescriptlang.org/) with [yarn]() as the package manager.

<strong>Note:</strong> The react version used with this app should be at most v16.

## Getting started <a name="getting-started"></a>

You can download the script zip on the GitHub release page.

Extract the zip contents to the folder of your choosing. Then on the command line navigate into the project folder and install the app dependencies by running the below command

```
yarn install
```

## Configurations <a name="configuration"></a>
### Source code configuration

These are in-app configurations that need to be done to initiate the connection with the DHIS2 instance during development. These configurations can be done by creating a `.env` file in the root directory of the project with contents similar to the `.env.example` files or as elaborated bellow

```
REACT_APP_DHIS2_BASE_URL=<base-url-for-app>
DHIS2_PROXY=<url-to-proxy-dhis2>
```
- <strong>REACT_APP_DHIS2_BASE_URL</strong> is the url that will provide a proxy to all the API requests to the DHIS2 instance. For example `http://localhost:8080`
- <strong>DHIS2_PROXY</strong> is the url where the actual DHIS2 is found so as to proxy it during development.

## Running the application <a name="run-app"></a>

The application can be run by running the below command at the root directory of the project:

```
yarn start
```

This runs the application and it can be accessible through the browser using: [http://localhost:3000](http://localhost:3000) address. Since the application uses ReactJs, it will be refreshing on files changes saving.

## Build and deployment <a name="build-deploy"></a>

To build and deploy the application, the following commands can be used respectively:

```
yarn build
yarn deploy

```

Check on these links for more information on [building](https://platform.dhis2.nu/#/scripts/build) and [deploying](https://platform.dhis2.nu/#/scripts/deploy).

<strong>Note: </strong> You must run `yarn build` before running `yarn deploy`.<br />
