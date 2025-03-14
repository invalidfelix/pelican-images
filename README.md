# Pelican-images

Docker images for Pelican, created on top of images from [Parkervcp](https://github.com/parkervcp/images), [Matthewpi](https://github.com/matthewpi/images)

## Guide

1. Create a perosnal access token on Github with use `write:packages` and `delete:packages` scope.
2. In the WSL workspace:

   ```
    export CR_PAT=TOKEN
    echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
   ```
   3. Navigate to the directory of the Dockerfile and build the image. The image should now show up in `Docker Desktop`.
      Make sure that line separators are set to `LF` for `entrypoint.sh`.Navigate to the directory of the Dockerfile and build the image. The image should now show up in `Docker Desktop`.
      ```
      docker build -t ghcr.io/USERNAME/IMAGE:TAG .
      ```
   4. Push the image to GitHub.
      ```
      docker push ghcr.io/USERNAME/IMAGE:TAG
      ```
