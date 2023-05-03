## 简介

本项目Fork自开源仓库[ChatGPT-Next-Web](https://github.com/Yidadaa/ChatGPT-Next-Web)，基于Vercel部署个人的ChatGPT网页服务，优点是服务器和域名是免费的，操作简单，可以在PC端和移动端使用。主要练习了Vercel的使用和ChatGPT官网OpenAI API Key的使用。

## 准备

+ 一个Vercel账户
+ 注册ChatGPT账号，在官网获取OpenAI API Key
+ 科学上网

## 主要内容

具体操作方法见[ChatGPT-Next-Web使用说明](https://github.com/Yidadaa/ChatGPT-Next-Web/blob/main/README_CN.md)。

注意在部署时候要设置一个访问密码和自己的OpenAI API Key。

## 效果展示

我部署的网页地址[chatgpt-next-web-pi-ecru.vercel.app](https://chatgpt-next-web-pi-ecru.vercel.app/)，登录秘钥可以私信联系。

由于vercel.app被DNS污染，国内无法访问，我又绑定了一个自己的域名[chatgpt.lijinning.top](https://chatgpt.lijinning.top)，该地址可以直接访问。

#### PC端界面

首页

![首页](https://raw.githubusercontent.com/L1468999760/chatgpt-next-web/main/pic/main.png)

在设置界面添加访问密码或者API Key

![设置](https://raw.githubusercontent.com/L1468999760/chatgpt-next-web/main/pic/key.png)

进行正常聊天

![聊天](https://raw.githubusercontent.com/L1468999760/chatgpt-next-web/main/pic/chatPC.png)

#### 移动端界面

用手机浏览器打开上面的网址后，会弹出添加桌面图标的提示，生成一个桌面图标。

<img src="https://raw.githubusercontent.com/L1468999760/chatgpt-next-web/main/pic/icon.jpg" width="100" height="100" />

首页

<img src="https://raw.githubusercontent.com/L1468999760/chatgpt-next-web/main/pic/start.jpg" width="300" height="600" />

聊天页面

<img src="https://raw.githubusercontent.com/L1468999760/chatgpt-next-web/main/pic/chat.jpg" width="300" height="600" />

## 其它应用

使用OpenAI API Key还可以做很多有趣的事情。

#### 代码翻译

> 参考开源项目[https://github.com/mckaywrigley/ai-code-translator](https://github.com/mckaywrigley/ai-code-translator)

将代码从一种语言翻译成另外一种语言。主要通过加入上下文信息，调用接口让AI实现翻译。

<img src="https://s2.loli.net/2023/05/03/fOWbiBV3gw5J8oN.png" width="540" height="400" >

如图所示，提前构造情景，让AI实现代码翻译功能，以下是效果展示：

<img src="https://s2.loli.net/2023/05/03/3ipvGmatB8OqVDK.png" >

我部署的服务地址，已经内置了秘钥，可以直接使用。

+ [code-translator.lijinning.top](https://code-translator.lijinning.top/)

#### ChatPDF

顾名思义，与PDF对话o(>_<)o。上传PDF文件后，向ChatGPT提问关于文件中的内容，AI给出回答。如果后续模型进一步增强，简直读论文神器哈哈。

基本原理：

+ 读取PDF文档，并对内容进行分割
+ 对于每段文本，使用Embedding模型生成特征向量
+ 将向量和文本对应关系存入本地文件
+ 对用户输入生成向量
+ 在数据库中进行最近邻搜索，返回最相似的文本列表
+ 设计Prompt（提示语），让ChatGPT基于最相似的文件列表给出回答

详细原理解释[How to Code a Project like ChatPDF?](https://postor.medium.com/how-to-code-a-project-like-chatpdf-e40441cb4168)

github上相关的代码很多，记录一个用的多的地址，需要科学上网访问。

+ [https://www.chatpdf.com/](https://www.chatpdf.com/)

<img src="https://s2.loli.net/2023/05/03/V2t8KkSTzxAMZaf.png" >

#### 真人对话

通过ChatGPT和Whisper语音识别，实现真人对话。

体验地址：

+ [https://huggingface.co/spaces/JavaFXpert/Chat-GPT-LangChain](https://huggingface.co/spaces/JavaFXpert/Chat-GPT-LangChain)

<img src="https://s2.loli.net/2023/05/03/jC7M9KhgmGvwWXn.png" >

