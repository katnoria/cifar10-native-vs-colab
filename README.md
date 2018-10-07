# Convnet Training Comparison

The recent announcement of TPU availability on Colab made me wonder the amount of time required to train a Convnet on various options available to me. In this repo, I have included the links to Colab notebook and the time taken on each runtime accelerator including the training time on my workstation.


|Notebook|Training Time (seconds)|
|<a href="">Local GPU</a>| 32|
|<a href="https://colab.research.google.com/drive/1UCMQJDpJ5hEiUEQ4qMAj0UBiYQ6n8Yg-">Colab GPU</a>| 86|
|<a href="https://colab.research.google.com/drive/1rP91Q5L1mPOVt7FcKkqFJSIMZrBtDawO">Colab TPU</a>| 136|

All three notebooks use the same network architecture, batch size and hyperparams. 

However, it is not a fair comparison because the notebook perhaps doesn't use the code optimized for target hardware, neither does it account for hardware differences between the local vs cloud VMs.

To me, I wanted to find out if whether I'll get any benefits if I just took my notebook from local machine to Colab. If I am using my laptop, that has AMD GPU, the anwser is yes I would definitely use Colab GPU. My code will run as in without needing any wrappers, as is the case with TPU. 


# Conclusion

We live in great times where compute and infra such as Google Colaboratory is accessible freely to anyone with internet connection. All you need is a laptop, desktop or even a piTop (haven't tried it) and you get instant access to a GPU or TPU.  
