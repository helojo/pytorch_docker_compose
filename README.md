# pytorch-docker-compose
## Features
:flashlight: **Base image jupyter/tensorflow-notebook:tensorflow-2.6.2**

:flashlight: **Libraries torch, torchvision, tensorboard installed from pip (last versions)**

:flashlight: **Torch device "cuda" (Linux only)**

:flashlight: **Port 8888 for JupyterLab, port 6060 for Tensorboard**

:flashlight: **Volumes from local directory**


## How to run
### Install Docker Engine, Docker Compose, NVIDIA Container Toolkit
Follow this guide: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html
### Clone repository
    git clone https://github.com/ScuOG/pytorch-docker-compose.git
### *(optional)* Set volumes
Edit docker-compose.yml

- Default sync based on current folder:
```
    - volumes:
      - ".:/home/jovyan/work"
```
- Sync specific folder:
```
    - volumes:
      - "~/Documents:/home/jovyan/work"
```
### Start
```
docker-compose up
```
Copy token from terminal

Open http://localhost:8888/lab and paste token

*(optional)*    Set dark theme: Settings > Theme > JupyterLab Dark

*(optional)*    Open "template.ipynb"
