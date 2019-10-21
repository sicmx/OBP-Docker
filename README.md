# Prenda-Clic-Docker

Files required to create the images available at Docker Hub https://hub.docker.com/r/sicmx/

## Build prendaclic-sicmx

    $ docker build --no-cache -f Dockerfile.prendaclic-sicmx -t sicmx/prendaclic-sicmx .

## Run prendaclic-full in docker container

    docker run -d -p 8080-8082:8080-8082                           \
    -e "ADVERTISED_HOST=localhost"                                 \
    -e "OBP_API_HOSTNAME=http://127.0.0.1:8080"                    \
    -e "OBP_BASE_URL_API_EXPLORER=http://localhost:8082"           \
    -e "OBP_BASE_URL_SOCIAL_FINANCE=http://localhost:8081"         \
    -e "OBP_WEBUI_API_EXPLORER_URL=http://localhost:8082"          \
    sicmx/prendaclic-sicmx
