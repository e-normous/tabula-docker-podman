# tabula-docker-podman
Containerfile and Dockerfile for starting a tabula container, accessible through a web browser. You either use it with podman or docker (see [here](https://github.com/asnelling/tabula-docker/tree/master) for inspiration).

**Manual when using podman on a raspberry pi 5**

1. Make sure [podman](https://podman.io/docs/installation) is installed
2. create a directory to store the Dockerfile or Containerfile from this Repo OR just clone the repo directly without creating a new directory
    > mkdir tabula-pdf
    
    > git clone https://github.com/e-normous/tabula-docker-podman.git
3. change into that newly created directory OR the cloned directory
    > cd tabula-pdf
    
    > cd tabula-docker-podman
4. build the image (e.g. with podman)
    > podman build . -t tabula-pdf-image
5. after building was successful, start the container (in detached mode and exposing port 8505 as EXPOSED in the Containerfile)
    > podman run -d -p 8505:8080 tabula-pdf-image
6. use the web application
    > http://localhost:8505
    
