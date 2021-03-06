# Fast.AI Setup
https://www.youtube.com/playlist?list=PLfYUBJiXbdtSLBPJ1GMx-sQWf6iNhb8mM

## Pre-requisites
Assuming using windows:
- get windows terminal (or Powershell)
- have windows 10 updated since (march?) 2020 for wsl2.

### Setup Linux terminal in windows
*HINT!* Remeber your [[Terminal|terminal commands ;)]]
1. In (windows/powershell) terminal, enter `wsl --install` or `wsl.exe --install`
2. Make sure installation of linux kernel is complete (in our case, Ubuntu). Computer restart required. 
3. UNIX user setup required. choose user and pw
4. _optional: update linx with `sudo apt update` and `sudo apt get`_
5. setup "git" and "downloads" directories in home directory `pwd` (go with with `cd`) using `mkdir git` and `mkdir downloads`

Troubleshooting internet connectivity issues:
- https://stackoverflow.com/questions/62314789/no-internet-connection-on-wsl-ubuntu-windows-subsystem-for-linux
- https://github.com/microsoft/WSL/issues/5336#issuecomment-653881695

 

## Setup python

### Install mamba
NEW METHOD  - old method redundant [^bignote]
1. go to [fastai/fsatsetup](https://github.com/fastai/fastsetup) and get url of raw view of "setup-conda.sh" 
2. In downloads directory in terminal, use `wget https://raw.githubusercontent.com/fastai/fastsetup/master/setup-conda.sh`
3. run `bash setup-conda.sh`

4. after installation is finished, restart shell and confirm `which python` returns 
``` 
/home/*USER*/mambaforge/bin/python or something similar 
```

[^bignote]: 
	OLD method (use NEW instead)
	1. find linux installation file mamba from https://github.com/conda-forge/miniforge
	2. In downloads directory in terminal, use `wget https://github.com/conda-forge/miniforge/releases/latest/download/Mambaforge-Linux-x86_64.sh`
	3. run `bash Mambaforge-Linux-x86_64.sh` and follow prompts to install mamba, choosing to initialise conda.init

### Install pytorch
https://pytorch.org/get-started/locally/
`conda install pytorch torchvision torchaudio cudatoolkit=11.3 -c pytorch`

### Install jupyter
`mamba install jupyterlab`

to stop no browser warning (as none is installed in Ubuntu)
`alias jl="jupyter lab --no-browser"`

## Install fast ai
`mamba install -c fastchan fastbook sentencepiece`