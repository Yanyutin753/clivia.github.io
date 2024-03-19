<div align="center">

# 🖼️ ChatGPT-ON-WeChat PictureChange插件

![GitHub stars](https://img.shields.io/github/stars/Yanyutin753/pictureChange?style=flat-square&label=Stars&logo=github) ![GitHub forks](https://img.shields.io/github/forks/Yanyutin753/pictureChange.svg?style=flat-square&label=Forks&logo=github)

✔ 借助 stable diffusion webui，实现图像的画图和生成 
✔ 可在企业微信、个人微信和微信公众号中使用

<br>
</div>

## 📌  插件描述

本插件主要提供以下功能特性：

- 对接百度AI进行图像处理
- 采用 stable diffusion webui 进行图像处理和绘制画图
- 支持多种 stable diffusion（简称 sd）模型
- 能够进行并发请求控制
- 管理员可以灵活修改 Host
- 提供自定义模板
- 管理员可以自由开启与关闭群聊及图生图功能
- 可在企业微信、个人微信及公众号中使用

## 🔧 环境要求

部署使用前，请先安装 stable diffusion webui，并添加 "--api" 至其启动参数，将其设置为 API 模式。

查看安装视频，请参考[这里](https://www.youtube.com/watch?v=Z6FmiaWBbAE&t=3s)。

部署运行后，请确保主机能正常访问此地址：http://127.0.0.1:7860/

如果是在服务器环境部署，无需配置内网穿透；若在本地电脑部署，建议使用[cpolar](https://dashboard.cpolar.com/signup)进行内网穿透。

在使用本插件前，请确保已**安装**所有依赖包。安装依赖，请执行以下命令：

```
pip3 install -r requirements.txt
```

## 🤖 使用方式

请先将 `config.json.template` 文件复制为 `config.json`，然后根据实际需求修改其中的参数和规则。

如：修改 pictureChange 的 `host`、`port`、`sd_model_checkpoint`、`api_key` 和 `secret_key`，并填写对应模型的名称。

### 图生图请求格式

#### 个人微信：

- 群聊：先发送"开启图生图"开启功能，之后群聊中的每一张图片都能被自动识别。如果不希望使用此功能，可发送"关闭图生图"进行关闭。
- 单聊：直接发送图片即可。

#### 公众号和企业微信：

- 直接发送图片即可使用插件功能。

### 更多功能

- 管理员一键开启或关闭图生图功能；
- 更改 Host（由于部署在内网，每次 IP 变动需要更改）；
- 分流控制：当请求数超过 3 的时候，会自动发送等待消息给用户，用户需要等待前面的任务完成后再发起新的请求。

### 部署操作
1. 确保 stable diffusion webui 部署成功且能正常访问
2. 解压安装包，只保留`pictureChange`文件夹在 plugins 目录里面。将 `config.json.template` 复制为`config.json`，并根据实际需求修改参数和规则。
3. 覆盖相应文件：

    对于个人微信：
    - 将 [chat_channel.py](https://github.com/Yanyutin753/wechat_pictureChange/blob/main/%E4%B8%AA%E4%BA%BA%E5%8F%B7/chat_channel.py) 覆盖 chatgpt-on-wechat\channel\chat_channel.py。
    - 将 [godcmd.py](https://github.com/Yanyutin753/wechat_pictureChange/blob/main/%E5%85%AC%E4%BC%97%E5%8F%B7%E5%92%8C%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1/godcmd.py) 覆盖 chatgpt-on-wechat\plugins\godcmd\godcmd.py。
    - 在根目录 config.json 和 config.py 分别添加如下代码：

    ```json
    "group_imageChange": true, 默认为 True
    "group_imageChange": False, 默认为 True
    ```

    对于公众号和企业微信：
    - 直接将 [godcmd.py](https://github.com/Yanyutin753/wechat_pictureChange/blob/main/%E5%85%AC%E4%BC%97%E5%8F%B7%E5%92%8C%E4%BC%81%E4%B8%9A%E5%BE%AE%E4%BF%A1/godcmd.py) 覆盖 chatgpt-on-wechat\plugins\godcmd\godcmd.py。

4. 安装依赖：进入 pictureChange 文件夹，运行 `pip3 install -r requirements.txt`。

### 贡献与支持

欢迎提交代码、提问和建议！如果你发现了 Bug 或有新的功能想法，欢迎提交 Issue。你也可以通过 Fork 项目并提交 Pull Request 来贡献代码。

如果你觉得这个项目好用，请给我一个星星作为鼓励吧！⭐

你的一份赞助，让我更有动力改进代码！感谢你的支持！

![image](https://github.com/Yanyutin753/wechat_pictureChange/assets/132346501/713eb69e-6e00-46ad-bec5-0b3926305ef0)

有问题可随时加入我们的讨论群组：

![2045e6eec4d1feebab7159b200154bd](https://github.com/Yanyutin753/pictureChange/assets/132