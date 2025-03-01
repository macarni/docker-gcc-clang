![screenshot](https://user-images.githubusercontent.com/65416560/214981016-21e61b0c-eaea-4d11-aabe-c7c5dedc92ff.png)

# Docker container with gcc and clang
Docker container based in ubuntu18 to compile with gcc7 and clang15
- zsh + p10k pre-configured
- mounts a volume in your preferred working directory so you can edit outside the container and compile and execute in it.
- specially developed for use in the 42 Madrid iMacs

## Requirements
- Docker installed and running
- `git clone https://github.com/yeta1990/docker-gcc-clang /sgoinfre/$USER/docker-gcc-clang`
- (optional) [MesloLGS font](https://github.com/romkatv/powerlevel10k#fonts)/[Nerd fonts] (https://github.com/ryanoasis/nerd-fonts#macos-os-x)installed

## Config
#### Replace environment variables in `srcs/.env` file: 
- DLC_WORK_VOLUME_ORIGIN: path of the folder where your code is in your host. i.e.: $HOME/Documents/libft
- DLC_WORK_VOLUME_DESTINATION: path of the folder where you will found your code in your container. i.e: /home/libft
- DLC_WORKING_DIR: path of the folder where you will enter when you open a new terminal of the container. i.e.: /home/libft

#### (at least in 42 iMacs) Docker desktop, Preferences->Resources:
- Advanced->Disk image location: /goinfre/your_user
- File sharing: /goinfre/your_user

## How to
- build and run the container: go to the main folder of this repository and type `make`. Make sure you have already edited the `config` file with your paths before you start building the container.
- open a terminal with the running container: type `docker exec -it ubuntu /bin/zsh`
- stop the container: `make stop`
- clean everything: `make fclean`
