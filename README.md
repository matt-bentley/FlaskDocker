# FlaskDocker
Production ready Docker image using Nginx, Gunicorn and Flask. The application will currently run on the standard host port (80) using Nginx and reverse proxy into port 5000 inside the Docker container where the flask application is hosted using a Gunicorn production ready server.

### Base Docker Image

* [ubuntu:16.04](https://registry.hub.docker.com/_/ubuntu/)

### Build From Dockerfile

Navigate to repository folder. nginx-gunicorn-flask can be changed to your own image name.

```bash
docker build -t nginx-gunicorn-flask .
```

### Usage

```bash
docker run -d -p 80:80 danriti/nginx-gunicorn-flask
```

After few seconds, open `http://<host>` to see the Flask app.

