# Masking
NIPS'18: Masking: A New Perspective of Noisy Supervision (Tensorflow implementation).

Introduction about the codes

------------------------------------------------------------------------------
Models:

(1) cifar10_train.py implements the classifier directly trained on the dataset.

(2) cifar10_train_T.py implements the loss correction method in https://github.com/giorgiop/loss-correction

(3) cifar10_train_varT.py implements the classifier with adaptation of noise transition.

(4) cifar10_train_GANT.py implements our MASKING model.

-----------------------------------------------------------------------------
Datasets:

(1) The CIFAR-10 dataset can be downloaded and placed in the corresponding position by following the introduction in ./data/cifar-10-batches-bin/readme.txt

(2) The noisy datasets is generated by noise.py based on the clean CIFAR-10 dataset. 

You can switch the noisy dataset for cifar10_train_T.py, cifar10_train_varT.py and cifar10_train_GANT.py by setting the NOISE_TYPE parameter in cifar10_input.py

-----------------------------------------------------------------------------
An example:
(1) Due to the requirements of initialization about the noise transition, some codes must be executed in order.
For example, you can execute the codes in the following codes,

python cifar10_train.py
python cifar10_train_T.py
python cifar10_train_varT.py
python cifar10_train_GANT.py

(2) For evaluation, since the evaluation scripts are separated, you can first launch up the training script and then launch up the evaluation script in another terminal.
For example,

python cifar10_train.py
python cifar10_eval.py


Contact: Jiangchao Yao (sunarker@sjtu.edu.cn); Bo Han (bo.han@riken.jp).
