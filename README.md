# Docker-Compose
## Nodejs Sample App With Nginx Reverse Proxy Connected to MongoDB Database

## Aims:
- To use docker-compose to connect the nodejs sample app with a mongodb server. This project included:
	- Using docker to create a container to run the nodejs sample app with the nginx reverse proxy
	- Using docker to create a container to run a mongodb server  
	- Using docker-compose to launch and connect these 2 containers

## Instructions:
- Run ``docker-compose up``
- This will launch and connect the 2 containers
- You can now access the blog page at ``localhost:3000/posts``

### Blog

``localhost:3000/posts``

This page displays a logo and 100 randomly generated blog posts. The posts are generated during the seeding step.

This page and the seeding is only accessible when a database is available and the DB_HOST environment variable has been set with it's location.

### Homepage

``localhost:3000``

Displays a simple homepage displaying a Sparta logo and message. This page should return a 200 response.
