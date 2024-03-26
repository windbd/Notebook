# 开源社区
- pytorch
- openXLab
- huggingface
- Alibaba——modelscope,easyNLP,easyCV
- Baidu——paddlepaddle,

# 开源项目
[Baichuan2基于ModelScope的推理和微调](https://pai.console.aliyun.com/#/dsw-gallery/preview/deepLearning/nlp/baichuan2_modelscope)
- 利用ModelScope中`SWIFT`框架对`Baichuan2-7B-Chat`模型进行微调
- 微调用的是`alpaca-en`和`alpaca-zh`数据
- 微调后在`advertise-gen`上进行推理
  
[Llama2-7B-Chat大模型的轻量化LoRA 微调及量化](https://pai.console.aliyun.com/#/dsw-gallery/preview/deepLearning/nlp/llama2_lora)
- 利用Meta的`llama-recipes`开源库，通过`PEFT`工具对`Llama2-7B`大模型进行微调
- 微调模型使用的训练数据集支持**自定义**
- 最后用int8对模型参数进行**量化**，从而使用更少显存进行推理
  
[EasyRec答疑机器人](https://pai.console.aliyun.com/#/dsw-gallery/preview/aigcHackathon/EasyrecQaRobot)
  - 通过问题检索**EasyRec**(推荐系统框架)相关文档、QA和参数，筛选并构建合理的prompt
  - 将prompt输入到`Qwen-7b-Chat`千问大模型中，实现自动化答疑
  - 直接运行会出现`AttributeError`，需要在`langchain.document_loaders.DirectoryLoader`的源代码中抛出异常

