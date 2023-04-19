# 一、环境
## Anaconda
- [怎么安装Anaconda3](https://zhuanlan.zhihu.com/p/75717350)
  
> 删除.condrac文件可以重置源环境路径
> 换源工具pqi可以把PyPi源迅速切换化为国内源
> 发现错误的包在文件夹中直接删除
> 根据包列表的后缀确定包安装的方式
> pip与conda在安装更新和卸载包时要对应
> dist-info文件夹是依赖库信息

```powershell
### 环境管理
>>conda create -n myenv python=3.5            
>>conda info -e                  
>>conda remove --name myenv --all   

>>conda env export > path/environment.yaml #导出环境
>>conda env create -f environment.yaml #导入环境

>>conda list --revisions #历史环境记录
>>conda install --revision [revision number] #恢复环境版本

### channels管理
>>conda config --show #查看chanel
>>conda config --add channels [channels] #添加channels
>>conda config –remove channels [channels] #删除channels

### 包管理
>>conda list #查看安装的包
>>pip install [packge]=x.x.x
>>conda install -c [packge]=x.x.x
>>pip uninstall [packge]
>>pip install --upgrade [packge]=x.x.x
>>conda uninstall [packge]
>>conda update [packge]=x.x.x

>>conda clean -p      //删除没有用的包(segment fault)
>>conda clean -t      //删除tar包
>>conda clean -y --all //删除所有的安装包及cache
```

## jupyter
- [jupyter notebook添加、删除内核](https://blog.csdn.net/I_LOVE_MCU/article/details/108311698)
- [jupyternotebook连接不上虚拟环境](https://blog.csdn.net/flyfish866/article/details/121221837)
- [jupyter notebook查看内存的使用情况](https://blog.csdn.net/bonjour001/article/details/121475500)
- [更改Jupyter Notebook的默认工作路径](https://zhuanlan.zhihu.com/p/59738776)
- [jupyter安装插件](https://blog.csdn.net/sinat_23971513/article/details/120102672)
- [jupyter lab 插件安装](https://blog.csdn.net/Fei20140908/article/details/119464205)
- [argparse模块如何在jupyter notebook中用于传参](https://zhuanlan.zhihu.com/p/145720581)
## Vscode
> python代码调用文件时是以终端中的打开的文件夹为根路径
> 在vscode中根路径是资源管理器中打开的最顶层的文件夹
> 
- [Vscode的相对路径读取问题及处理](https://blog.csdn.net/sumaliqinghua/article/details/90404173)
- [VSCODE 设置不可见文件的隐藏，特定文件不显示在文件列表中](https://blog.csdn.net/qq_41554005/article/details/117926256)
- [VSCode 连接远程服务器上的 Jupyter 环境](https://zhuanlan.zhihu.com/p/508764623)
# 二、库包
## pytorch
- [为什么电脑装了pytorch没有安装cuda，还是能够使用gpu？](https://www.zhihu.com/question/378419173)

>Nvidia CUDA：`CUDA toolkit`、CUDA driver、NVIDIA GPU driver
>CUDA:驱动API和运行API
>驱动API是显卡驱动支持的最高cuda版本，用`nvidia-smi`查看
>运行API是`CUDA Toolkit`的版本，Anaconda包含CUDA的运行API
>pytorch的cuda版本的算力不低于机器上显卡的算力
>pytorch的cuda的版本不高于机器上显卡驱动的cuda版本
>`torch.cuda.empty_cache()`与`gc.collect()`

```python
### pth,pt,pkl文件 
# 模型参数保存与调用
torch.save(model.state_dict(),mymodel.pth) #权重参数
model = My_model(*args, **kwargs)
model.load_state_dict(torch.load(mymodel.pth)) #调用模型参数
# 模型保存与调用
torch.save(model,mymodel.pth)
model=torch.load(mymodel.pth)
```
## NLP库
- [NLTK下载错误的终极解决办法](https://blog.csdn.net/u010099177/article/details/102900515)
- [Tokenizer快速使用](https://zhuanlan.zhihu.com/p/548347360)
> **torchtext的安装：**
> pytroch的的版本为1.a.b，则torchtext的版本为0.(a+1).b
> 若pytorch == 1.13.1，则`pip install torchtext == 0.14.1`

## CV库
- [Pytorch视觉模型库--timm](https://blog.csdn.net/qq_42003943/article/details/118382823)

# 三、基础应用

## 基础知识
- [python字符串前加r、f、u、l](https://blog.csdn.net/sinat_38682860/article/details/108884655)

## 应用开发
- [python实现API的调用](https://blog.csdn.net/qq_42370313/article/details/121869032)
- [BeautifulSoup全面总结](https://zhuanlan.zhihu.com/p/35354532)
- [更简单高效的HTML数据提取-Xpath](https://www.cnblogs.com/pywjh/p/9708264.html)
- [基于Python获取亚马逊的评论](https://blog.csdn.net/CorGi_8456/article/details/122579206)
- [pytorch GPU分布式训练 单机单卡、单机多卡](https://blog.csdn.net/hihui1231/article/details/127605644)
