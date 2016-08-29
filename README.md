# Autograder Sandbox

This Python library uses Docker container functionality to create a secure, isolated environment for running untrusted code.

## Installation
Currently, installation must be done manually.

1. Install [Docker](https://docs.docker.com/engine/installation/)
1. Install Redis (this is used to allow separate processes spawning containers to use distinct linux user IDs in their containers)
1. Add the source code to your project (If using Django, be sure to add 'sandbox' to your installed apps).
1. In a terminal running docker, run `docker build -t autograder /path/to/autograder_sandbox/docker-image-setup`
1. To run the tests, run `python3 -m autograder_sandbox.tests`

## Configuration
By default, the sandbox program tries to connect to Redis at localhost:6379. To change the host or port, set the AG_REDIS_HOST
and AG_REDIS_PORT environment variables, respectively.
