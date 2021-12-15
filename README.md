# dockerLinkedContainersTest

This is a very simple project showcasing some basic familiarity with docker.

It consists of 3 main linked containers:
- `client` - spins up a local development server, whilst mounting the existing `node_modules` folder if any, to reduce spin up times. The production `DockerFile` is also backed by another nginx container that redirects asset requests appropriately.
- `server` - spins up a local server handling api calls, backed also by a redis container.
- `nginx` - rewrites and proxies requests to the above 2 containers as appropriate
