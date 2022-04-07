# Quick MySQL Server built with Docker Compose

A basic mysql server built using Docker Compose. It consists of the following:
* MySQL

As of now, I have several different MySQL versions. Use appropriate MySQL version as needed:

* 5.7
* 8.0

##  Installation
 
* Clone this repository on your local computer
* configure .env as needed 
* Run the `docker-compose up -d`.

```shell
git clone https://github.com/cybergitt/quick-mysql-server
cd quick-mysql-server/
cp sample.env .env
// modify sample.env as needed
docker-compose up -d
```

Your MySQL Server is now ready!! 

##  Configuration and Usage

### General Information 
This Docker Stack is build for local development and not for production usage.

### Configuration
This package comes with default configuration options. You can modify them by creating `.env` file in your root directory.
To make it easy, just copy the content from `sample.env` file and update the environment variable values as per your need.

### Configuration Variables
There are following configuration variables available and you can customize them by overwritting in your own `.env` file.

---
#### Environments
---

_**DATABASE**_

Define which MySQL or MariaDB Version you would like to use. 

_**MYSQL_INITDB_DIR**_

When a container is started for the first time files in this directory with the extensions `.sh`, `.sql`, `.sql.gz` and
`.sql.xz` will be executed in alphabetical order. `.sh` files without file execute permission are sourced rather than executed.
The default value for this is `./config/initdb`.

_**MYSQL_DATA_DIR**_

This is MySQL data directory. The default value for this is `./data/mysql`. All your MySQL data files will be stored here.

_**MYSQL_LOG_DIR**_

This will be used to store Apache logs. The default value for this is `./logs/mysql`.

## Greetings
Thank you! 
