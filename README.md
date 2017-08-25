## Overview
This is a simple set up for test driving Scala Spark scripts. It is fairly portable, as all you need to use it are:
- `docker` version 17.06.1-ce or greater
- `docker-compose` version 1.14.0 or greater
- Intellij Ultimate/Community edition 2017.2 or greater

## Using
Build tools and test dockers
```sh
docker-compose build
```

If you would like to use the tools that the docker uses for testing, compiling, etc. run
```sh
docker-compose run tools
```
And it will place scala (including sbt) and linux/osx JDK 8 versions in a `tools` folder for you to use

Now you can run the tests via your IDE (after adding your own JDK, scala and sbt or the ones provided in the `tools` folder)

-or-

Run them via docker-compose, which takes some time as it does a clean sbt run every time
```sh
docker-compose run test
```
