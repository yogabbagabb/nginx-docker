# Dockerized Flask Server behind Nginx Proxy


## Description

This repository contains the code needed to build a docker image that:

- Runs flask in production mode
- Runs flask behind an Nginx reverse proxy

This is a minimum working example (MWE) of the code needed to dockerise a flask app in a production setting.

## Usage

Prerequisites:

- Have the ability to execute `docker` from your CLI.

```
docker build . -t flask_image
```

builds the image and names it `flask_image`.

```
docker run --name flask_container -p 80:80 flask_image
```

runs a container named `flask_container` off the aforementioned image.


## Credits

A significant amount of this code was sourced from a blog post by [Alexey Smirnov.](https://smirnov-am.github.io/running-flask-in-production-with-docker/)