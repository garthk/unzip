# unzip

`unzip`, in a Docker container.

Usage, if you're very trusting:

    docker run --rm -v $PWD:/unzip garthk/unzip whatevs.zip

Usage, if you're less trusting:

    curl -OL https://raw.githubusercontent.com/garthk/unzip/master/Dockerfile
    less Dockerfile
    docker build -t unzip .
    docker run --rm -v $PWD:/unzip unzip whatevs.zip

Notes:

* The working directory, from `unzip`'s point of view, defaults to `/unzip`

* Use `--volume` or `-v` to bind-mount to the ZIP file and to the source or
  destination directory

* `:ro` can be used to bind-mount read-only, e.g. `-v $PWD:/unzip:ro`
