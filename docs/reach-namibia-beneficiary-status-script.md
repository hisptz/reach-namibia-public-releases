# REACH Namibia Beneficiary Status Script

## Introduction

This script automates the process of assigning beneficiaries to different programs in the REACH program in Namibia. The programs include:

- DREAMS
- Male engagement
- Preventive OVC
- Caregiver
- Comprehensive OVC

The assignments are based on the services provided to the beneficiaries within a given time frame, using criteria specific to each program. This script ensures that beneficiaries are correctly categorized based on their received services, making program management more efficient and accurate.

## Tooling

This script uses the following basic packages as basic toolings:

- Commander: This is a tool to improve the script user experience when using the
  script. [Learn more](https://www.npmjs.com/package/commander)
- Winston: A tool for logging different information within the
  script. [Learn more](https://www.npmjs.com/package/winston)
- Axios: A HTTP client for accessing DHIS2 API resources Or any http
  resources. [Learn more](https://www.npmjs.com/package/axios)
- Luxon: A javascript package for manipulating time. [Learn more](https://www.npmjs.com/package/luxon)
- Lodash: A javascript package for manipulating objects and arrays. [Learn more](https://www.npmjs.com/package/lodash)

## Dependencies

Since this is a node script, it needs [Node](https://nodejs.org/en) to be installed together with a package manager of preference between [npm](https://www.npmjs.com/) and [yarn](https://yarnpkg.com/).

## Getting started

## Setting up 
You can download the script zip in the GitHub release page.

Extract the zip contents to the folder of your choosing

### Installing packages

Packages can be installed using `npm` Or `yarn` using bellow commands:

```
npm install
```

Or

```
yarn install
```

### Setting environment variables

Environment variables can be set by creating `.env` file with contents similar as `.env.example` Or as shown below:

```
DHIS2_BASE_URL=
DHIS2_USERNAME=
DHIS2_PASSWORD=
EVALUATION_PERIOD_ID=
SENDGRID_API_KEY=
SENDGRID_FROM_ADDRESS=
EMAIL_RECIPIENTS=
```

Note:

- Below is the definition of the above variables:
  - DHIS2_BASE_URL: This is the url to the DHIS2 instance.
  - DHIS2_USERNAME: This is the username for accessing the DHIS2 instance.
  - DHIS2_PASSWORD: This is the password for accessing the DHIS2 instance.
  - EVALUATION_PERIOD_ID: This is the period type for evaluating the script. For example, THIS_QUARTER or THIS_MONTH.
  - SENDGRID_API_KEY: This is the API key from Sendgrid for sending the emails.
  - SENDGRID_FROM_ADDRESS: This is the email address for sending the emails using sendgrid.
  - EMAIL_RECIPIENTS: This is the list of comma separated emails who will be receiving the script summary.

### Starting development server

The development server can be started using the command:

```
yarn beneficiary-status
```

or

```
npm run beneficiary-status
```

### Building the script

The script can be built using the following commands:

```
yarn build
```

or

```
npm run build
```
