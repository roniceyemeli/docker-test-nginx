## Dockerize React App

- npx create-react-app
- create the Dockerfile
- create the .dockerignore file
- run the container
- create production build 
- serve it with nginx
#### Commands
```sh
 #this will build our react-app image
docker build --tag dockerizereactapp . 
 # to run our react-app as a container
docker run -p 8080:3000 dockerizereactapp
#serve your static build artifacts through a Nginx webserver, which of course, is also dockerized.
docker build -t dockerizereactapp:nginx -f Docker_prod .
```