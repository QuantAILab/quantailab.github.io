# QuantAI

## News

Start of reconstruction from a more professional aspect of financial analysis.

## Setup

Base env setup:

```shell
# Install Anaconda3
## Download Anaconda
wget https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh

## With Default Configuration is OK.
bash Anaconda3-2020.11-Linux-x86_64.sh

## Source
source ~/.bashrc

# Create Python Environments
conda create -n QuantAI python=3.7 -y

# Config GitHub Account
git config --global user.name densechen
git config --global user.email densechem@foxmail.com

# Rewrite
ssh-keygen -o

# Copy to git ssh-key access
cat ~/.ssh/id_rsa.pub
chmod 0600 ~/.ssh/id_rsa
```

Clone and install repo:

```shell
export WORK_DIR=/media/sata/share/Project
# activate current env
conda activate QuantAI

for repo in [ 'contrib' 'QuantAI' 'QuantBase' 'QuantDB' 'datac' 'datad' 'source' 'QuantSpider' 'QuantUI' 'Starry' 'Aurora' 'QuantAgent' 'Quanter' 'Nebula' 'QuantText' 'QuantRec' 'Polaris' 'transaction' ]; then 
do
    cd $WORK_DIR
    echo "Downloading {$repo}"
    git clone git@github.com:QuantAILab/{$repo}.git
    echo "Building {$repo}"
    cd $repo && bash setup.sh
done

```

## Docker

A ready-to-use docker image will be released.
