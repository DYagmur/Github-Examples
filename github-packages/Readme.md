export GH_USERNAME='DYagmur'
export GH_TOKEN=''
export GH_IMAGE_NAME='hello-world'
export GH_VER='1.0.0'

export TAG_NAME="ghcr.io/$GH_USERNAME/$GH_IMAGE_NAME:$GH_VER"


echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag hello-world:latest ghcr.io/dyagmur/hello-world:1.0.0

docker push ghcr.io/dyagmur/hello-world:1.0.0

docker 

LABEL org.opencontainers.image.source https://github.com/OWNER/REPO 

