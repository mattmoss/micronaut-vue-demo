# Simple Micronaut Vue Demo

The server sub-project includes a Micronaut service for managing
Person instances in a relational database.

The ui sub-project includes a Vue front end which communicates
with the Micronaut service.

To run the services you will need to have JDK 8 or later
installed and configured.


## Running Locally

Run the server:

```
./gradlew :server:run
```

After the server starts run the ui:

```
./gradlew :ui:run
```

After the ui starts up, open a browser and send a request
to http://localhost:8081 to access the UI.

The server is configured to use an in memory database so
the data will disappear when the process is terminated.



## Building Bundled Server

To build a standalone executable jar to serve up both
the ui and the REST api, execute the assemble task:

```
./gradlew assemble
```

Or to assemble and run tests, execute the build task:

```
./gradlew build
```


## Running Bundled Server

To run the standalone jar:

```
./gradlew runShadow
```

Or to run the standalone jar without gradle:

```
java -jar server/build/libs/server-0.1-all.jar
```

After the server starts up, open a browser and send a request
to http://localhost:8080 to access the application.
