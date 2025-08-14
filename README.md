# tabula-docker-podman
Containerfile and Dockerfile for starting a tabula container, accessible through a web browser.

**Manual when using podman on a raspberry pi**

1. Make sure [podman](https://podman.io/docs/installation) is installed
2. create a directory to store the Dockerfile or Containerfile
    > mkdir tabula-pdf
3. change into that directory
    > cd tabula-pdf
4. clone this repo
    > git clone
5. build the image (e.g. with podman)
    > podman build . -t tabula-pdf-image
6. after building was successful, start the container
    > podman run -d -p 8505:8080 tabula-pdf-image
7. use the web application
    > http://localhost:8505
    
