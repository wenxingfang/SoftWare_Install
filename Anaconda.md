## Login lxslc7
## Download Miniconda (light than Anaconda) : https://docs.conda.io/en/latest/miniconda.html?source=post_page--------------------------- 
## Install conda : bash Miniconda3-latest-Linux-x86_64.sh
## Update conda ? (maybe don't do it, it causes error)
## Set the PATH 
## conda init
## conda create -n myenv
## conda activate myenv
## conda deactivate
## conda install -c anaconda keras-gpu (or keras)
## If want to run tensorflow or keras in lxslc6 or lxslc7 locally, need set:
```js
import tensorflow as tf
session_conf = tf.ConfigProto(
      intra_op_parallelism_threads=1,
      inter_op_parallelism_threads=1)
sess = tf.Session(config=session_conf)

###### or ################3

from keras import backend as K
import tensorflow as tf
config = tf.ConfigProto(intra_op_parallelism_threads=args.jobs, \ 
                        inter_op_parallelism_threads=args.jobs, \
                        allow_soft_placement=True, \
                        device_count = {'CPU': args.jobs})
session = tf.Session(config=config)
K.set_session(session)
```
