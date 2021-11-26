# Step-to-step for Running Chroma on Windows

## Step 1 - Preparation & Set Up GPU

Need a machine with an NVIDIA GPU
Install Python, Docker Desktop, VSCode

In Windows -> settings, go to Windows insider and get Windows 11.
Then follow https://docs.docker.com/desktop/windows/wsl/
(Here I'm using Ubuntu 20.04)

If get "Error: only 0 Devices available, 1 requested. Exiting." when running
```sh
docker run --rm -it --gpus=all nvcr.io/nvidia/k8s/cuda-sample:nbody nbody -gpu -benchmark
```
Reboot


## Step 2 - Run Chroma with GPU

Download Chroma (https://github.com/BenLand100/chroma) (using chroma3:nvidia)

Add Chroma to Python,
```sh
python3
import sys
sys.path.append(<your dir containing chroma, bin, etc.>)
exit()
```

In Ubuntu, pull and run image by creating a container
```sh
docker pull benland100/chroma3:nvidia
docker run --name nvidia -it --gpus=all benland100/chroma3:nvidia
```

Next time, one can start the container by
```sh
docker start nvidia --interactive
```
and can stop running by
```sh
docker stop nvidia
```

Then run the file by
```sh
python3 <file name>.py
```

