# TALLER-5-MLOPS
## Share Docker Image

You can share an image without Docker Hub by saving it to a file and loading it later:

- [docker save](https://docs.docker.com/reference/cli/docker/image/save/)  
  ```bash
  docker save -o image.tar my_image:tag
  ```

- [docker load](https://docs.docker.com/reference/cli/docker/image/load)  
  ```bash
  docker load -i image.tar
  ```

## With this Docker Image
```bash
docker save -o pipeline.tar diego2250/taller-5-mlops:latest
docker load -i pipeline.tar
```

## Conclusions
- Requirements or Conda help recreate environments but can still break with system differences.  
- Pickle files only move the model, not the whole setup.  
- Docker runs the same everywhere since it includes code, deps and OS.