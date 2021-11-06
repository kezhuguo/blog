# Step-to-step Instructions on Installing Chroma on Windows

## Step 1 - Preparation & Set Up GPU

Need a machine with an NVIDIA GPU
Install Python, Docker Desktop, VSCode
Download Chroma (https://github.com/BenLand100/chroma) and follow the instructions to run the image (using chroma3:nvidia)

In Windows -> settings, go to Windows insider and get Windows 11.
Then follow https://docs.docker.com/desktop/windows/wsl/
(Here I'm using Ubuntu 20.04)

If get "Error: only 0 Devices available, 1 requested. Exiting." when running
```sh
docker run --rm -it --gpus=all nvcr.io/nvidia/k8s/cuda-sample:nbody nbody -gpu -benchmark
```
Reboot


## Step 2 - Install Chroma

(Go to chroma-master -> doc -> source -> install)
(Here's the instruction for Ubuntu 20.04 in particular:)

Install system packages:
```sh
sudo apt-get install python3-pygame python3-matplotlib python3-virtualenv build-essential xorg-dev python3-dev libglu1-mesa-dev  freeglut3-dev uuid-dev liblapack-dev mercurial git subversion libatlas-base-dev libbz2-dev
```

CUDA Toolkit and Driver:
```sh
sudo service gdm3 stop
wget https://developer.download.nvidia.com/compute/cuda/11.5.0/local_installers/cuda_11.5.0_495.29.05_linux.run
sudo sh cuda_11.5.0_495.29.05_linux.run

sudo service gdm3 start
```

TODO: install nvidia driver...(sudo apt install nvidia-driver-495)


Open $HOME
```sh
sudo apt install xdg-utils
xdg-open .
```
In .profile, add
```sh
export PATH=/usr/local/cuda/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda/lib64/:$LD_LIBRARY_PATH
```
check in kernel
```sh
echo $PATH
```

TODO: continue to common installation

```sh
```




