# Docker-react-node
Your <b>React.js</b> environment in just one command using <a href="https://github.com/facebookincubator/create-react-app">create-react-app</a>, node, mongo and yarn into a docker container.

## Docker && docker-compose installation instructions:

Install <b>docker</b> and <b>docker-compose</b> in your host machine:

* Follow Docker installation guide: <a href="https://docs.docker.com/engine/installation">https://docs.docker.com/engine/installation</a>
* Follow Docker-compose installation guide: <a href="https://github.com/docker/compose/releases">https://github.com/docker/compose/releases</a>

Extra recommended optional step for allowing linux non-root users to run docker commands:
* `$ sudo usermod -aG docker $USER`

## Build and start your React environment with single command:

Just run:

* `$ docker-compose up` you will see two containers: one for node-react (port 3000) and another for mongo (port 27019)

* To gracefully stop undetached run just press CTRL+C

## Test your React Installation:

* Check your code at src/ 
* Open http://localhost:3000

## Docker-compose basic handling:

Run in detached mode:

* `$ docker-compose up -d`

In detached mode, you won't have direct output from the container, so you'll have to check the container logs to see if the build ended (find the above "Compiled successfully" message):

* `$ docker-compose logs`

Stop a detached mode run:

* `$ docker-compose down`

Run commands into your container without going into, from your host machine:

* `$ docker-compose exec docker-react-node mycommand`

Enter into your container to run commands inside it (ssh-like):

* `$ docker-compose exec docker-react-node bash`

Exit your container, and go back to your host machine:

* `$ exit`
