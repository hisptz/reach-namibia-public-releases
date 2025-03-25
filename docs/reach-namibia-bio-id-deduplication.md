# REACH NAMIBIA BIO ID DEDUPLICATION SCRIPT

## Introduction

This is a node script that removes the duplicate Bio IDs from the Reach Namibia program. It follows the guidelines for deduplicating the Bio IDs as specified by the program team.

## Tooling

This script uses the following basic packages as basic toolings:

- Commander: This is a tool to improve the script user experience when using the
  script. [Learn more](https://www.npmjs.com/package/commander)
- Winston: A tool for logging different information within the
  script. [Learn more](https://www.npmjs.com/package/winston)
- Axios: A HTTP client for accessing DHIS2 API resources Or any http
  resources. [Learn more](https://www.npmjs.com/package/axios)
- Luxon: A javascript package for manipulating time. [Learn more](https://www.npmjs.com/package/luxon)

## Getting started

### Setting up 
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
DHIS2_BASE_URL=<url-for-dhis2-instance>
DHIS2_USERNAME=<dhis2-username>
DHIS2_PASSWORD=<dhis2-password>
```

### Running the script

The script can be run using either `npm` Or `yarn` as show bellow:

- Running deduplication for the current day data:

```
npm run deduplication daily
```

Or

```
yarn deduplication daily
```

- Running deduplication for all the system data

```
npm run deduplication all
```

Or

```
yarn deduplication all
```

## Building

The script can be build using `npm` Or `yarn` as show below:

```
npm run build
```

Or

```
yarn build
```
