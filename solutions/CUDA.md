* 我的情况
  * 在安装CUDA之前，已经安装过tensorflow，但尚未安装pytorch
* 安装过程
  * CUDA：首先去NVIDIA官网，直接下载了最新版本的CUDA 11.6，一路下一步，安装完成，记得使用extras文件夹下的几个工具验证CUDA安装；
  * cuDNN：官网最高版本只支持CUDA 11.5，强行安装最新版本，事实证明和CUDA 11.6没有问题
  * pytorch：官网找到安装命令，显示支持CUDA 11.3，其实是支持CUDA 11.3以上版本的CUDA（在官网安装文档靠下的位置，可以看到）
    * pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113
    * ~~~Python
      torch.cuda.current_device()
      torch.cuda.device(0)
      torch.cuda.device_count()
      torch.cuda.get_device_name(0)
      ~~~
  * tensorflow
    * tensorflow2.x 不再区分CPU版本和GPU版本
    * 由于我之前已经安装过tensorflow，支持使用`tf.test.is_gpu_available()`测试，返回False
    * 查询资料，普遍反映CUDA版本不对导致该问题
    * 但重新安装CUDA有点点麻烦，死马当活马医，卸载tf重新安装，发现可以找到GPU了