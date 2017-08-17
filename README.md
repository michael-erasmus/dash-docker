# docker-dash

An easy way to get started with [dash](https://plot.ly/products/dash/) using Docker.

## Usage

Start a dash server with the [getting started example](https://plot.ly/dash/getting-started)  

```
docker run --rm -it --net=host michaelerasmus/dash
```

To start with your own app, create a `app.py` and mount the current directory
```
docker run --rm -it --net=host -v "$PWD":/usr/src/myapp michaelerasmus/dash
```

Building the image locally:

```
git clone https://github.com/michael-erasmus/dash-docker
cd dash-docker
docker build -t michaelerasmus/dash .
```

Using a custom `Dockerfile`:

```Dockerfile
FROM michaelerasmus/dash

#Customize things here
```
