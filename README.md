# myjupyterlab
## crear intancia en EC2
turorial: https://dataschool.com/data-modeling-101/running-jupyter-notebook-on-an-ec2-server/

sudo apt update
sudo apt upgrade

## install anaconda

wget https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Linux-x86_64.sh

## add path for anaconda
export PATH=/home/ubuntu/anaconda3/bin:$PATH

## Step 6: Configuring Jupyter Notebook settings
First, you need to create our Jupyter configuration file. In order to create that file, you need to run:

jupyter notebook --generate-config

conf = get_config()

conf.NotebookApp.ip = '0.0.0.0'
conf.NotebookApp.password = u'YOUR PASSWORD HASH'
conf.NotebookApp.port = 8888

jupyter notebook password
