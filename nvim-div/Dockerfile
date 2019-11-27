FROM alpine

# Update and install
RUN apk update
RUN apk --update add curl gcc g++
RUN apk --update add neovim
RUN apk --update add git 

# python settings
RUN apk --update add python python-dev python3 python3-dev
RUN curl -kL https://bootstrap.pypa.io/get-pip.py | python
RUN python -m pip install neovim
RUN python3 -m pip install --upgrade pip
RUN python3 -m pip install neovim

# add mysettings
WORKDIR /root/.config
RUN git clone https://github.com/sn-mtsmt/nvim.git

WORKDIR /root

