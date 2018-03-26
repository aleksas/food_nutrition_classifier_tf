# pip

Either build environment using requirements.txt or requirements_gpu.txt using pip  (e.g. pip install -r  requirements.txt)

# Docker

## Build container
Build a docker image using following command `docker build -t "food_nutrition_classifier:dockerfile" . -f Dockerfile.gpu` .

## Pull container
`docker pull food_nutrition_classifier:dockerfile`


## Run container
### GPU
nvidia-docker run -i -t -p 8888:8888 -p 6006:6006 food_nutrition_classifier:dockerfile
### CPU
docker run -i -t -p 8888:8888 -p 6006:6006 food_nutrition_classifier:dockerfile
