# pytorch_docker_compose
## Features
:flashlight: **Base image:**

&emsp;&emsp;&emsp;&emsp;jupyter/tensorflow-notebook:tensorflow-2.6.2

:flashlight: **Packages from pip:**

&emsp;&emsp;&emsp;&emsp;torch, torchvision, tensorboard

:flashlight: **Torch device:**

&emsp;&emsp;&emsp;&emsp;cuda (Linux only)

:flashlight: **Ports:**

&emsp;&emsp;&emsp;&emsp;8888 for JupyterLab, 6006 for TensorBoard

:flashlight: **Volumes:**

&emsp;&emsp;&emsp;&emsp;sync from local directory
## How to run
### Install Docker Engine, Docker Compose, NVIDIA Container Toolkit
Guide for Linux: https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html
### Clone repository
    git clone https://github.com/ScuOG/pytorch-docker-compose.git
### *(optional)* Set volumes
Edit "docker-compose.yml"

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
cd pytorch-docker-compose
docker-compose up
```
Copy token from terminal

Open http://localhost:8888/lab and paste token

*(optional)*    Set dark theme: Settings > Theme > JupyterLab Dark

*(optional)*    Open "template.ipynb"
