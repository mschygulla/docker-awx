# docker-awx

This repository contains a docker-compose definition to run the multi-container Docker application for [AWX](https://github.com/ansible/awx).

AWX provides a web-based user interface, REST API, and task engine built on top of Ansible.

## Usage

Start AWX:

    docker-compose up -d

Stop AWX:

    docker-compose stop

Upgrade AWX:

    docker-compose pull && docker-compose up --force-recreate

Tail the awx_task log:

    docker logs -f awx_task

## Accessing AWX

The AWX web server is accessible on the deployment host, using the port value set in the docker-compose.yml file. The default URL is http://localhost.

Login with ```admin``` and password ```password```

## Where is the Data stored

The default data directory of this multi-container Docker application is ```./awx```.

## License

View [license information](https://github.com/ansible/awx/blob/devel/LICENSE.md) for the software contained in this image.