# PostgreSQL + Meteor

Adds postgres support to Meteor via `SQL.Collection`, which is similar to
`Mongo.Collection` and provides the same functionality namely livequery, pub/sub, latency compensation and client side cache.

Still I would not recommend using it in production yet as the ORM layer is open for SQL-injections.

### TODOS

Exeption Handling

### Installation

Run the following from your command line.

```
    meteor add kkappel:meteor-postgres
```

or add this to your `package.js`

```
    api.use('kkappel:meteor-postgres');
```

### Usage

To get started you might want to take a look at the todo-example
code. You can run the code by cloning this repo locally and start it by running
`MP_POSTGRES=postgres://{username}:{password}@{host}:{port}/{database} meteor` 
inside the cloned directory.

### Tests

To run the test execute the following from your command line.

```
MP_POSTGRES=postgres://{YOUR USERNAME ON THE MACHINE}:numtel@localhost:5439/postgres JASMINE_SERVER_UNIT=1 VELOCITY_TEST_PACKAGES=1 meteor --port 4000 test-packages --driver-package velocity:html-reporter storeness:meteor-postgres
```

and check on [localhost:4000](http://localhost:4000)

### Implementation

We use [Node-Postgres](https://github.com/brianc/node-postgres) on the server and [AlaSQL](https://github.com/agershun/alasql) on the client.
Also thanks to [Meteor-Postgres](http://www.meteorpostgres.com/) as this project
is based on their initial work, but which gets not longer maintained.

### License

Released under the MIT license. See the LICENSE file for more info.
