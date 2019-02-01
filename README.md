# Convnet Training Comparison

The recent announcement of TPU availability on Colab made me wonder the amount of time required to train a Convnet on various options available to me. In this repo, I have included the links to Colab notebook and the time taken on each runtime accelerator including the training time on my workstation (**NVIDIA 1080TI**).


|Notebook|Training Time (seconds)|
|--------|-----------------------|
|<a href="https://github.com/katnoria/cifar10-native-vs-colab/blob/master/CIFAR10_Keras_GPU.ipynb">Local GPU (1080Ti)</a> or [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/katnoria/cifar10-native-vs-colab/master?filepath=CIFAR10_Keras_GPU.ipynb)| 32|
|<a href="https://colab.research.google.com/drive/1UCMQJDpJ5hEiUEQ4qMAj0UBiYQ6n8Yg-">Colab GPU (Tesla K80)</a>| 86|
|<a href="https://colab.research.google.com/drive/1rP91Q5L1mPOVt7FcKkqFJSIMZrBtDawO">Colab TPU</a>| 136|

All three notebooks use the same network architecture, batch size and hyperparams. 

However, it is **not a fair comparison** because it doesn't take the hardware, video card, vram etc into account and neither is the code in notebook optimized for target hardware. Using a local workstation with good NVIDIA GPU works best but with Colab we are free from the troubles of cuda installations/upgrades, environment management or package management. 

To me, I wanted to find out if whether I'll get any benefits if I just took my notebook from local machine to Colab. If I am using my laptop, that has AMD GPU, the anwser is yes I would definitely use Colab GPU. My code will run as is, without needing any wrappers. TPU Accelerator on the other hand does require wrapping the model around contrib.tpu and does not seem to support eager mode yet. But I expect these to go away as TPU moves from contrib into core. 


# Conclusion

We live in great times where compute and infra such as Google Colaboratory is accessible freely to anyone with internet connection. All you need is a laptop, desktop or even a piTop (haven't tried it) and you get instant access to a GPU or TPU.  
