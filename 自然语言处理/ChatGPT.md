# chatGPT准备工作

### 科学上网
- 由于ChatGPT没有开放国区，所以需要一个可以魔法上网的工具，保证自己可以访问ChatGPT官网
- 参考教程：[最新 Clash for Windows 使用教程快速入篇](https://clashforwindows.org/ "最新 Clash for Windows 使用教程快速入门篇")

### 国外邮箱
- 目前ChatGPT对于邮箱要求还是比较高的，国内邮箱（QQ、163等）无法使用
- 可以用Gmail、Proton等国外邮箱注册

### 国外手机号
- openAI平台需要使用手机号验证登录，国内的手机号无法验证，所以我们还需要准备一个国外手机号，这个可以用接码平台来实现
- 用到的接码平台的网站（后面有具体的参考使用方式的网站：[sms-activate](https://sms-activate.org/ru "sms-activate")

### 用邮箱注册
- 进入[openAI首页](https://chat.openai.com)，点击Sign UP开始注册
- 使用前面准备的邮箱进行注册，需要在邮箱中进行登录验证

### 手机号验证
- 通过手机验证，这里要用到国外手机号，首先在接码平台进行注册
- 接着在平台购买手机号并在openAI填入限时的手机号
- 最后将平台返回的验证码输入到openAI进行验证
- 参考教程：[最新ChatGPT注册教程](https://chatgptzh.github.io/how-to-register-a-chatgpt-account-in-china/ "最新ChatGPT注册教程")

### chatGPT plus(GPT 4)
- 相比于普通版，plus采用更多的数据进行训练，且采用了更大的模型，因此plus可以生成更高质量的文本，让您获得更广泛的知识和理解
- 开通使用教程：[国内开通Chat GPT Plus保姆级教程](https://chatgpt-plus.github.io/chatgpt-plus/ "国内开通Chat GPT Plus保姆级教程")

# chatGPT的API

### 申请API
- 登录OpenAI官方账号，进入官方的[API平台](https://platform.openai.com/)
- 点击右上角View API keys—> Create new secret keys生成自己的API keys（只显示一次）
- openAI给新注册的用户提供了$5美元的免费token使用，有时间的限制
- 如果需要大量使用API接口，需要绑定国外的信用卡进行充值，参考教程:[国内ChatGPT API Key申请使用及虚拟信用卡充值教程](https://chatgpt-plus.github.io/chatgpt-api-key/#%E4%B8%80%E3%80%81ChatGPT-API%E4%BB%8B%E7%BB%8D)

### API参数
- 可以在openai的Playground中进行测试查看

|参数|解释|
| :------------ | :------------ |
|Mode|使用的模式，包括chat、Complete、Edit|
|Model|这里可以切换模型，不同的模型会擅长不同的东西|
|Temperature|控制回复的随机性。值越高,回复越具有创造性和多样性,但也更偏离提示的内容。默认值是 1|
|Top-p|控制生成文本的多样性，采样会从累积概率达到p以上的词集中采样，默认top-p为0，准确的答案，可以将它设定为较低的值|
|Max tokens|控制每个回复的最大词数|
|Stop sequence|如果生成的文本包含这些终止词,则会停止生成|
|Presence penalty|惩罚重复话题和论点。值越高,生成的回复越不重复。默认值为 0|
|Frequency penalty|惩罚重复使用相同的词。值越高,重复词使用越少。默认值为 0|
- 大多数模型的最大字符的限制为4096个tokens（包含输入+输出），比如输入4095个tokens，chatGPT只回复你一个tokens

### API的调用
- 使用openAI官方API调用：用python通过openai库调用;用request等库调用API接口;官方教程[API Reference](https://platform.openai.com/docs/api-reference)
- 使用第三方封装SDK调用：第三方基于官方SDK进行了封装，使其更加易用；比如huggingface：[ChatGPTwithAPI](https://huggingface.co/spaces/ysharma/ChatGPTwithAPI)
- 具体的调用参数的说明可以参考playground的参数

# chatGPT的应用
### 外部应用
- WebChatFPT(插件)：实时将互联网搜到的内容传输给ChatGPT进行回答
- MaxAI(插件)：在任意的网页与不同的AI大模型对话
- chathub(插件)：同时和不同的AI大模型对话
- chatPDF(网站)：可以分析PDF文件内容；官方网站：[chatPDF](https://www.chatpdf.com/)
- Poe(网站)：访问不同公司的AI工具；官方网站：[Assistant - Poe](https://poe.com/)
- AutoGPT(项目)：在本地或服务器上搭建，发现无法解决的问题时，自动网络搜索答案；教程：[炸裂的 AutoGPT，鱼皮教你免费用](https://zhuanlan.zhihu.com/p/624577366)
### LangChain
- LangChain是一个围绕LLMs（大语言模型）建立的框架，使用机器学习算法和海量数据来分析和理解自然语言。它的核心理念是为各种LLMs实现通用的接口，把LLMs相关的组件“链接”在一起，简化LLMs应用的开发难度，方便开发者快速地开发复杂的LLMs应用LangChain目前有两个语言的实现：`python`和`nodejs`
- LangChain的应用场景包括：基于文档的问答、聊天机器人、代理、信息提取、文档总结等
- Langchain支持多种大模型，包括但不限于GPT-3、GPT-2、Bert、chatGLM等
- Langchain的官方网站：[LangChain](https://www.langchain.com/)
- Langchain的中文网站：[LangChain中文网](https://www.langchain.com.cn/)
- Langchain的中文社区：[LangChain中文社区](https://www.langchain.cn/)

# Prompt

### prompt介绍
- 指导人工智能执行任务的过程称为prompt，我们向 AI 提供一组instruction（prompt），然后它执行任务
- 通过学习 prompt 可以让你更好地使用 ChatGPT 等产品
- 基于LangChain的prompt结构模板：
	- Instruction（必须）： 指令，即你希望模型执行的具体任务
	- Context（选填）： 背景信息，或者上下文信息，这可以引导模型做出更好的反应
	- Input Data（选填）： 输入数据，告知模型需要处理的数据
	- Output Indicator（选填）： 输出指示器，告知模型我们要输出的类型或格式

- prompt的原则
	- Prompt 里最好包含完整的信息
	- Prompt 最好简洁易懂，并减少歧义
	- 要使用正确的语法、拼写，以及标点

### prompt使用
- 问题问答：告诉模型你要干什么，或者告诉模型不能干什么来缩小范围
- 基于示例问答：无法用文字准确解释问题或指示，可以在prompt里增加一些案例
- 推理：比如解决数学问题
- 内容生成：写代码、招聘信息、朋友圈等
- 内容改写：翻译、修改、润色，可以在prompt里增加一些role相关的内容，让内容更符合需求
- 内容总结：考虑增加总结的示例或者考虑增加角色，使用特殊符号`"""XXXXX"""`将指令和文本分开
- 信息提取：通过格式词阐述需要输出的格式







