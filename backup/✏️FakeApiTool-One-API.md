<div align="center">

#  ✏️[FakeApiTool](https://github.com/Yanyutin753/fakeApiTool-One-API)

![GitHub stars](https://img.shields.io/github/stars/Yanyutin753/fakeApiTool-One-API?style=flat-square&label=Stars&logo=github) ![GitHub forks](https://img.shields.io/github/forks/Yanyutin753/fakeApiTool-One-API.svg?style=flat-square&label=Forks&logo=github)
![](https://img.shields.io/badge/license-MIT-blue.svg)
## 基于 [One API](https://github.com/songquanpeng/one-api) 和 [Pandora](https://ai.fakeopen.com/) 中的 [FakeApi](https://ai.fakeopen.com/) 的高效工具，旨在以更简便的方式使用[pandora](https://ai.fakeopen.com/)资源，让你能便捷地享受 chatGPT
</div>



## 🌈概要
**[FakeApiToo](https://github.com/Yanyutin753/fakeApiTool-One-API)** 是一款基于 [One API](https://github.com/songquanpeng/one-api) 和 [Pandora](https://ai.fakeopen.com/) 中的 [FakeApi](https://ai.fakeopen.com/) 的高效工具，旨在以更简便的方式使用[pandora](https://ai.fakeopen.com/)资源，让你能便捷地享受 chatGPT。本工具是以伟人为基石，为广大使用者创造便利，欢迎给予我们鼓励和支持！

## ⚠️注意事项
- 在使用本工具前，请务必先安装并启动 One-API，并确保 One-API 已接入 SQL！

### Docker启动 One-API
此处，我们提供了一个用于启动 One-API 的 Docker命令，需要注意的是，你需要在下面的命令中填写好你的 One-API 数据表的密码。具体命令如下：

```bash
docker run --network="host" --name one-api -d --restart always -p 3000:3000 -e SQL_DSN="oneapi:YOUR_PASSWORD@tcp(localhost:3306)/oneapi" -e TZ=Asia/Shanghai -v /home/ubuntu/data/one-api:/data justsong/one-api 
```

## 🔮 功能特性
- **保存账号信息：** 支持保存 OpenAI 账号密码和 token，方便快速访问。
- **自动获取 API keys：** 工具可以自动获取 One-API 的 API keys，省去手动获取的步骤。
- **自动添加删除修改渠道：** 工具能够自动在 One-API 中添加删除修改渠道，简化配置过程。
- **每日自动更新渠道请求地址：** 工具会每日自动更新渠道的请求地址，确保始终使用最新的数据。
- **每五天自动通过openAI账号密码刷新token,更新渠道：** 工具会每五天自动通过openAI账号密码刷新token,更新渠道，方便使用。

### 初始用户名：root 初始密码值:123456
初次使用后，建议将账号密码更改为 One-API 的账号密码。

## ⭐鼓励
如果你觉得我的项目对你有所帮助，那就请给我们一个赞吧！非常感谢你的支持！

## 📣声明
本项目依托于 [One API](https://github.com/songquanpeng/) 以及 [Pandora](https://ai.fakeopen.com/) 的资源，我们衷心感谢这两大的贡献者！同时，我们也欢迎有志之士一同来帮助我们改进这个项目，让它变得更方便，更简单！

> 大家好，我是 ⭐，如果你喜欢我，请不吝赠送我一个！