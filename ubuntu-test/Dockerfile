FROM ubuntu:latest
RUN apt update && apt upgrade -y
### notes to remind the purpose for each tools installed #####
#net-tools: ifconfig
##############################################################
RUN apt install -y vim \ 
				   git \
				   net-tools \
				   python3 \
				   python3-pip \
				   cmake \
				   lsb-release \
				   curl
#clone required repositories
RUN mkdir -p ~/.repos
RUN git clone https://github.com/bonohub13/vim_settings ~/.repos/vim_settings
RUN git clone https://github.com/morhetz/gruvbox ~/.repos/gruvbox
RUN git clone https://github.com/bonohub13/docker_test_env_ubuntu20.04 ~/.repos/docker_test_env_ubuntu20.04
RUN mkdir ~/.vim
#vim settings
RUN cp -r ~/.repos/gruvbox/colors ~/.vim
RUN cp ~/.repos/vim_settings/.vimrc ~/
#ros1 install
RUN . ~/.repos/docker_test_env_ubuntu20.04/ros1-installer/installer.bash
