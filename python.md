## Login lxslc6.ihep.ac.cn, (may also can be done in lxslc7)
## cd /workfs/higgs/fangwx
## Install Python : follow the introduction here: https://my.bluehost.com/hosting/help/python-install
### Before go to next step, make sure "which python" gives you own python location. 
## Install pip : curl https://bootstrap.pypa.io/get-pip.py | python - --user , this will install pip to ~/.local/bin
  ### See https://askubuntu.com/questions/889535/how-to-install-pip-for-python-3-6-on-ubuntu-16-10
  ### Add ~/.local/bin to PATH
### Install virtualenv (if you want) : python -m pip install --user virtualenv
## Add /workfs/higgs/fangwx/python/Python-3.6.6/build/lib.linux-x86_64-3.6 to PYTHONPATH
## Set PIP_TARGET=/path/to/pip/install/ . (Note: can't use with --user) this can set the path of pip installed packages.
## Add $PIP_TARGET to PYTHONPATH
## Install tensorflow: pip3 install --upgrade tensorflow-gpu
### It seems better to switch to lxslc7, otherwise there will be some problem. in lxslc7 need type 'klog' once.
### Test: import tensorflow as tf
### To solve glibc raised problem (no problem if you are in lxslc7): https://zhuanlan.zhihu.com/p/33059558, dowload the glibc here : http://ftp.gnu.org/gnu/glibc/glibc-2.17.tar.gz
## Finall install keras: pip install keras

# Install PyTorch
### https://pytorch.org/get-started/previous-versions/
### conda create -n pyTorch_v1p2_py37 python=3.7
### conda activate pyTorch_v1p2_py37
### conda install -c conda-forge numpy
### conda install pytorch==1.2.0 torchvision==0.4.0 cudatoolkit=10.0 -c pytorch
### done

# Install faiss
### https://github.com/facebookresearch/faiss/wiki/Getting-started
### conda create -n Faiss_py3p7 python=3.7
### conda activate Faiss_py3p7
### conda install faiss-gpu cudatoolkit=10.0 -c pytorch

# Install MMdnn
### https://github.com/microsoft/MMdnn
### conda create -n MMdnnV1_py37 python=3.7
### conda activate MMdnnV1_py37
### pip install mmdnn
### conda install tensorflow-gpu==1.14 pytorch==1.2.0 torchvision==0.4.0 cudatoolkit=10.0 -c pytorch



