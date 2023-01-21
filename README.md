
# Piranha JLink Hello World template

This project delivers you with a template to get started with Piranha Embedded
and JLink. 

## Building locally

To build the project locally use the following Maven command line:

```shell
  mvn clean install
```

## Executing the custom JLink runtime

As part of the build the project will create a custom JLink runtime. After 
building the project you will find it in the `target/jlink` directory. If you
want to try it out execute the wrapper in `target/jlink/bin/helloworld` And then
browse to `http://localhost:8080` to see it in action.

## Docker image with JLink runtime

### Creating a Docker image with the JLink runtime

If you want to deploy the JLink runtime using a Docker image you can execute
the following command line:

```shell
  docker build -t jlink .
```

This will create a Docker image named `jlink` you can then push to a Docker
registry or execute locally using Docker.

### Executing the Docker image with the JLink runtime

Once you have completed the previous section executing the Docker image is as
simple as the command line below.

```shell
  docker run --rm -it -p 8080:8080 jlink
```

And then browse to `http://localhost:8080` to see it in action.
