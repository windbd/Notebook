# 开源主页

- [my github homepage](https://windbd.github.io/)
- 
- [Professor Yi Yang](https://yya518.github.io/)  
- [Professor Tafseer Nayeem](https://tafseer-nayeem.github.io/)
- [Professor Liqiang Nie](https://liqiangnie.github.io/)
- [Professor Yang Deng](https://dengyang17.github.io/)
- 
- [Ph.D. Bowen Yin](https://bowenyinis.github.io/)
- [Ph.D. Beyond Hsueh](https://amourwaltz.github.io/)
- [Ph.D. Wenxuan Zhang](https://isakzhang.github.io/)
- [Ph.D. mengtingwan](https://mengtingwan.github.io/)
- 
- [Jeremy Feng](https://jeremy-feng.github.io/)
- [鹤啸九天](https://wqw547243068.github.io/)  
- [老刘说NLP](https://liuhuanyong.github.io/)  
- [deep learning for economists](https://econdl.github.io/)
- [Lilian](https://lilianweng.github.io/)

# 开源数据
## 词向量
- [Chinese Word Vectors 中文词向量](https://github.com/Embedding/Chinese-Word-Vectors)
- [MTEB排行](https://huggingface.co/spaces/mteb/leaderboard)
## 数据集
- [国家生态数据中心资源共享服务平台](http://www.nesdc.org.cn/)
- [jmcauley亚马逊数据集](https://cseweb.ucsd.edu//~jmcauley/datasets.html)
- [Yelp Dataset](https://www.yelp.com/dataset)
- [知识类问答数据集资源对外开放：百万级百度知道、社区问答及六大领域级小规模语料](https://mp.weixin.qq.com/s/j8-4Z2bGgvvv_WSmPcJbsw)
- [Stack Exchange Data Explorer](https://data.stackexchange.com/)
- [Stack Overflow数据](https://archive.org/download/stackexchange)
- [千言：NLP中文开源数据集](https://www.luge.ai/#/)
- [中文医疗信息处理评测基准CBLUE](https://tianchi.aliyun.com/dataset/95414)
- [Software Engineering Open Science Portal](https://openscience.us/)
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
