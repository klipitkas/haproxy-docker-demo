# HA-Proxy / Docker scaling demo
This is just an example on how load balancing can be achieved using HAProxy and Docker containers.

## Deployment and testing
- Clone this repository. 
- Build the docker image using: `docker build . -t awesome:latest` in order to tag the image file that will be created.
- Run `docker-compose up -d`. This should get you up and running with a single HAProxy instance and a single NodeJS server instance.

## Scaling
- In order to test the scaling capabilities you can run the following command after the docker containers are up:

`docker-compose scale awesome=AMOUNT_OF_NODEJS_INSTANCES`

## Monitoring
- Use the following credentials: `admin/admin` in order to login to http://localhost:1936
- You will now be able to see the running backend instances.
