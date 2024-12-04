The assignments are written in python.
Here is reported how to create a python virtual environment to run the code.
Using a Python virtual environment isolates project dependencies, preventing conflicts and ensuring consistent behavior across different projects.

Here is shown how to create the virtual environment on Linux
## Pre-requisites
### Install pyenv
```bash
sudo apt update && sudo apt upgrade

# python prereqs
sudo apt-get install build-essential gdb lcov pkg-config \
libbz2-dev libffi-dev libgdbm-dev libgdbm-compat-dev liblzma-dev \
libncurses5-dev libreadline6-dev libsqlite3-dev libssl-dev \
lzma lzma-dev tk-dev uuid-dev zlib1g-dev curl

sudo apt install libusb-dev make git avr-libc gcc-avr \
    gcc-arm-none-eabi libusb-1.0-0-dev usbutils

# install pyenv - skip if already done
curl https://pyenv.run | bash
echo 'export PATH="~/.pyenv/bin:$PATH"' >> ~/.bashrc
echo 'export PATH="~/.pyenv/shims:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init -)"' >> ~/.bashrc
echo 'eval "$(pyenv virtualenv-init -)"' >> ~/.bashrc

source ~/.bashrc
```
### Create a virtual environment
In this case the python venv is named `sca_venv`, but you can choose any name you like.
```bash
pyenv install 3.9.5
pyenv virtualenv 3.9.5 sca_venv
pyenv activate sca_venv
```
## Initiating the virtual environment
Any time you want to work on the project, you need to activate the virtual environment.
```bash
pyenv activate sca_venv
```
Check for other info here: 
https://chipwhisperer.readthedocs.io/en/latest/index.html#overview
