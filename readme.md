# Notes

## Prerequisites

* PostgreSQL 9.6 or later
* Node.js v10.15.1 LTS or later
* Grunt 1.0.0 or later
* Chrome


## Setup

####Brew Init
1. brew install postgresql
2. brew services start postgresql


###Init

1. Run `./setup.sh` to install dependencies.
2. Run `./init.sh` to initialize the database. It creates `notes` user, and `notes_development` and `notes_test` databases on PostgreSQL running locally.
3. Run `grunt init` to create users to login the Web app.


## Run

1. Run `grunt runServer` to run the server.
2. Visit http://localhost:7428/ with your browser. You can login using the information below.

    * Username: user1
    * Password: password1

    You can also login as user2/password2 and user3/password3.


## Test

* Run `grunt test` to test the code.
* Run `grunt coverage` to test the code with code coverage. Check `./coverage` directory to see the coverage.

You need Chrome to run the unit tests.


## Directories

* etc/ - Configurations
* public/ - Client
    * src/ - Client code
    * test/ - Client test
* src/ - Server code
    * api/ - Express router for APIs
    * app/ - Express router for app
    * domain/ - Domain classes implementing business logic
    * model/ - Model classes based on Sequelize
    * router/ - Utilities for routers.
* test/ - Server test
* tools/ - Some tools
