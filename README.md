# docker-downloads

Docker container to download an exe from a localhost url on port 8000
Project started by following this write up: -https://www.linkedin.com/pulse/serve-static-files-from-docker-via-nginx-basic-example-arun-kumar

# Building

docker build -t docker-static .

# Running

docker run --rm -i -p 8000:90 docker-static

    --rm    removes the code from the stopped container
    -i      interactive mode
    -p      publish the container's port (90) to the host (8000)

# Changing the file to download

Put the desired file to download in the /web/files folder.
Add the file type to the /mime.types file if not already there
The index on line 10 of /nginx.conf should point to the file that is to be downloaded
