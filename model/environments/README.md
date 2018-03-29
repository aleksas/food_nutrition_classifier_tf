# Prepare environment using pip

## CPU
`pip install -r  requirements.txt`

## GPU
`pip install -r requirements_gpu.txt`

# Prepare docker container (RECOMMENDED)

## Build container

### CPU
`docker build -t "food_nutrition_classifier:cpu" . -f Dockerfile`
### GPU
`docker build -t "food_nutrition_classifier:gpu" . -f Dockerfile.gpu`

### Serve model
`docker build -t "food_nutrition_classifier:serve" . -f Dockerfile.serve`

## Run container

### GPU
`nvidia-docker run -i -t -p 8888:8888 -p 6006:6006 food_nutrition_classifier:cpu`
### CPU
`docker run -i -t -p 8888:8888 -p 6006:6006 food_nutrition_classifier:gpu`
### Serve model
`docker run -i -t -p 9000:9000 food_nutrition_classifier:serve`
