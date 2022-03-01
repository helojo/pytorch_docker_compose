# pytorch-docker-compose
:flashlight: Python version:	 3.9.7

    Base image jupyter/tensorflow-notebook:tensorflow-2.6.2 (edit Dockerfile for specific image)

:flashlight: Torch version:	 1.10.2+cu102

    Last versions of torch, torchvision, tensorboard installed from pip (edit Dockerfile for specific versions)

:flashlight: Torch device:	 cuda

    Compatibility Linux only

:flashlight: Port 8888 for JupyterLab, port 6060 for Tensorboard

:flashlight: Volumes from local directory


## How to run
### Install Docker Engine, Docker Compose, NVIDIA Container Toolkit
Follow this guide: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html

### (Optional) set volumes by editing docker-compose.yml:
Default sync based on current folder:
```
    - volumes:
      - ".:/home/jovyan/work"
```
Sync specific folder:
```
    - volumes:
      - "~/Documents:/home/jovyan/work"
```
### Start:
```
docker-compose up
```

- copy token from terminal
- open http://localhost:8888/lab and paste token
