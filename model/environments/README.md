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
Replace `YOUR_SHARED_DIRECTORY` with path to the directory this repo was cloned to.
From inside container `cpu` or `gpu` container run `jupyter notebook --ip='*'`.

### GPU
`nvidia-docker run -i -t -v YOUR_SHARED_DIRECTORY:/tmp/model -p 8888:8888 -p 6006:6006 food_nutrition_classifier:gpu`
### CPU
`docker run -i -t -v YOUR_SHARED_DIRECTORY:/tmp/model -p 8888:8888 -p 6006:6006 food_nutrition_classifier:cpu`
### Serve model
`docker run -i -t -v YOUR_SHARED_DIRECTORY:/tmp/model -p 9000:9000 food_nutrition_classifier:serve`
