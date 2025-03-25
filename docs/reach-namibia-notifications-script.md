# Reach Namibia Notification Script

## Introduction

A script to disseminate app notifications based on referral activity in the Project Hope Namibia system

## How to use
This script is intended to be used on the same server as the DHIS2 instance. It is to be run periodically.
Running using `pm2` is highly recommended. A `pm2` configuration has been provided.

## Setting up 
You can download the script zip in the GitHub release page.

Extract the zip contents to the folder of your choosing

First create an `.env` file with values as indicated in the `.env.example` file.

You can then run the installation script 

```shell
 ./install.sh
```
or 

```shell
source install.sh
```
You can then check if the installation was successful by running 

```shell
phn-notifications --version
```

To run the script, use:

```shell
 phn-notifications
```

You can also use 

```shell
phn-notifications --help
```
to see further options


## Scheduling
To schedule the script to run at a given interval, you can either set up a cron job or use `pm2`
To use pm2, make sure it is installed;

```shell
  pm2 --version
```
If it is not installed, you can install it by running 

```shell
yarn global add pm2 
```
or 

```shell
npm install -g pm2
```
Then make sure it is enabled at startup 

```shell
pm2 startup
```

And then run:
```shell
pm2 start pm2.config.js
```
This will run the script after every 10 minutes. If you would like to change the interval, edit the cron found in the `pm2.config.js` file

```shell 
    nano pm2.config.js
```

```js
module.exports = {
	apps: [
		{
			name: "phn-notifications",
			script: "phn-notifications",
			cron_restart: "*/5 * * * *", //<= Change this to the desired cron
			watch: false,
			autorestart: false
		}

	]
};

```

And then restart the pm2 job;

```shell
pm2 restart phn-notifications
```

## Issues

If you encounter any issues or would like to recommend features open an issue on the
project's [issues](https://github.com/hisptz/reach-namibia-notifications-script/issues) page.
