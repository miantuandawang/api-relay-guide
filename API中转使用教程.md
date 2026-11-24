# API中转使用教程

[https://api.miantuan.ltd/]()

API中转站提供的API可用于国内网络环境不翻墙使用Codex Cli、Codex App及Opencode、OpenClaw等，当然也可用于在Python代码中调用API。

## 如何安装codex cli/app？

如果您有翻墙/梯子，强烈建议上官网直接安装codex app，根据您的系统下载即可。

[https://openai.com/zh-Hans-CN/codex/]()

对于codex cli，您需要先安装Node\.js

[http://nodejs.org/zh-cn?utm_source=chatgpt.com]()

安装完成Node\.js后，打开终端，输入

```Bash
node -v
npm -v
```

查看是否正确安装。

接着输入以下命令，并等待安装（这一步最好挂梯子）

```Bash
npm install -g @openai/codex
```

安装完成后，输入

```Bash
codex
```

即可打开codex cli，此时您尚未配置API，打开后可按ctrl\+c先退出，按照下面操作进行配置。

如果您在输入安装命令时卡住，建议使用阿里云镜像，也即下面这个命令

```Bash
npm install -g @openai/codex --registry=https://registry.npmmirror.com
```

## 如何在Codex Cli和Codex App中使用面团API？

### 使用开源软件CC switch帮助管理（方法一，推荐）

非常推荐使用CC swtich，您可以随意地切换不同中转站/官方的订阅，保持本地长久会话不被破坏。

首先安装CC switch
https://ccswitch\.io/zh/

![image\.png](图片和附件/image%201.png)

下面讲一下如何导入我们的某个密钥配置

首先进入你的账号，然后创建API key。

这里点击“创建密钥”

![image\.png](图片和附件/image%206.png)

这里选择codex分组即可（如您之后订阅了套餐，请新建密钥选择套餐的专属分组）

![step\_3\.png](图片和附件/step_3.png)

![step\_4\.png](图片和附件/step_4%201.png)

接着点击“导入到CCS”这个按钮。

![image\.png](图片和附件/image%204.png)

允许即可！

这里点“导入”确定。

OK，我们现在有两个配置了。

可以改一下名，比如我把刚导入的改为test，然后点击启动，就可以自动切换密钥啦！（这里的查询失败是bug，不影响）

如果您还有官方订阅（或其他中转站），可以点击右上角的➕号

选择Openai Official

![image\.png](图片和附件/image%203.png)

点击添加

![image\.png](图片和附件/image%2012.png)

再点击启用官方订阅。

随后打开中转，随便找个文件夹，输入codex logout。

![image\.png](图片和附件/image%208.png)

出现successfully logged out之后，再输入codex，利用网页认证登录您的gpt账号即可，会话将不会消失。

![image\.png](图片和附件/image%2011.png)

如您需要切换回中转站，可以点击中转站的启用即可。

### 

首先进入你的账号，然后创建API key。

![step\_1\.png](图片和附件/step_1.png)

这里点击“创建密钥”

![step\_2\.png](图片和附件/step_2.png)

这里选择codex分组即可（如您订阅了套餐，请新建密钥选择套餐的专属分组）

![step\_3\.png](图片和附件/step_3%201.png)

![step\_4\.png](图片和附件/step_4.png)

这里点击使用密钥

![step\_5\.png](图片和附件/step_5.png)

复制弹出的界面的两个配置，记住相对应的路径（如果没有该名字文件，则创建文件），然后把内容直接全部复制进去，保存即可。

![step\_7\.png](图片和附件/step_7.png)

下面演示一下mac电脑如何找到这个文件夹和目录

#### macos/linux配置

首先打开访达，找到这个小房子图标，也就是Home目录，点进去。

![image\.png](图片和附件/image%2010.png)

这个时候你还看不到名字叫\.codex的文件夹，所以需要按command\+shift\+\.（也就是“\.”这个键！！），这样你就能看到隐藏文件夹\.codex了，咱们点进去。

如果你这一步之后还是没在隐藏文件夹找到\.codex文件夹，说明你codex还没初始化，请先打开一次codex或者打开一次cli创建文件夹。

![image\.png](图片和附件/image%202.png)

可以看到这两个我们需要的文件了（如果没有请自己创建这两个同名文件）。

![image\.png](图片和附件/image.png)

把我们的内容复制进去配置完成后直接在终端

```Bash
codex
```

或者直接打开codex app即可使用codex cli或者codex app了，记得重启一下。

后续可以在Codex cli（输入指令/model）或者codex app（直接在对话框下面选择切换）切换模型为gpt\-5\.5，现在默认配置是选择gpt\-5\.4。

![image\.png](图片和附件/image%207.png)

若您是winodws或者linux系统，配置方法也类似，如您还存在其他问题，可以优先询问一下Deepseek，也欢迎在群内咨询～

#### windows配置

对于windows系统，可以直接按Win键\+R键，然后输入%userprofile%\\\.codex并直接回车，可以直接打开\.codex目录。

![image\.png](图片和附件/image%205.png)



## 部分报错及解决方法

1\.

![fbd3493d3bd8246017d5af88d4156bec\.jpg](图片和附件/fbd3493d3bd8246017d5af88d4156bec.jpg)

出现这个情况大概率是你config\.toml中自动压缩的窗口大小设置的不合理

建议改成这样，就不会出现这种问题了

![image\.png](图片和附件/image%209.png)

2\.

![132784da2942f4ad43f350f764de2b38\.png](图片和附件/132784da2942f4ad43f350f764de2b38.png)

这说明您现在的密钥所在分组下额度不足，如果您刚开通了订阅套餐，请新建一个该订阅分组下的密钥，然后用CC switch切换即可。



文档原作者：喵api miaoapi

