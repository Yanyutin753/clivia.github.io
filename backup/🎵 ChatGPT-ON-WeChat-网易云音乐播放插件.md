<div align="center">

<h1 align="center">🎵 ChatGPT-ON-WeChat 网易云音乐播放插件</h1>

![GitHub Repo stars](https://img.shields.io/github/stars/Yanyutin753/chatgpt-wechat-singSong?style=large)


</div>

## 🔌 适用于ChatGPT-on-WeChat项目的插件
这是一个用于在您的应用中播放网易云音乐的插件，通过利用网易云音乐的API，能够实现播放指定音乐、用户登录与VIP音乐的播放功能。并且，您可以参考[网易云api](https://neteasecloudmusicapi.vercel.app/#/)，进一步拓展更多的功能。

## 💡 功能特性
- 🗂 采用自己部署的[网易云音乐的API](https://github.com/Binaryify/NeteaseCloudMusicApi)。
- 🎧 输入音乐ID或链接来播放指定音乐。
- 👤 实现用户登录功能，可以登录自己的网易云音乐账号。
- 🎵 提供VIP音乐的播放，让音乐享受无障碍。
- 👩‍💻 开发友好，可以根据网易云音乐的API文档，进行更多的功能开发。

## 🛠 安装与使用
1. ⚙ 需部署[网易云音乐的API](https://github.com/Binaryify/NeteaseCloudMusicApi)（推荐使用Vercel部署，详见[详细文档](https://github.com/Binaryify/NeteaseCloudMusicApi)）。
2. 📥 下载插件并添加到`plugins`文件夹，或通过`godcmd`安装：`#installp https://github.com/befantasy/singsong.git`。
3. 🔧 在`config.json.template`文件中修改API地址，并将文件重命名为`config.json`。
4. ⚖ 公众号的语言需要微信审核，对付审核的时间可能较长，因此你可以参考[WeChatmp.channel](https://github.com/Yanyutin753/chatgpt-wechat-singSong/blob/main/%E6%9D%82%E9%A1%B9/wechatmp_channel.py)里的代码进行修改。

## 🔑 登录
登录有三种途径：
- 管理员登录，在`godcmd`插件添加相应的代码。[具体可参考下面文档](https://github.com/Yanyutin753/chatgpt-wechat-singSong/blob/main/%E6%9D%82%E9%A1%B9/godcmd.py.temp)
- 用户直接输入登录信息，通过扫描二维码进行登录。
- 通过浏览器访问你们部署的网站加`/qrlogin.html`进行登录。
你可以根据需求，自行修改代码，按需登录。

## 👀 使用情况
![进度周报](https://github.com/Yanyutin753/chatgpt-wechat-singSong/assets/132346501/27017915-1d7c-4413-a8fe-b04cc2c3b652)

![日志统计](https://github.com/Yanyutin753/chatgpt-wechat-singSong/assets/132346501/794c3699-5e8d-45f9-96df-5f01bfcf45a0)

![日志详情](https://github.com/Yanyutin753/chatgpt-wechat-singSong/assets/132346501/29000ddf-db40-4948-aef6-85ff0129ba09)

## 👏 贡献与支持
欢迎你的贡献，包括提出问题和建议，修复bug或增加新的功能。可以通过提交Issue或Pull Request来贡献你的智慧。如果你喜欢这个项目，欢迎给它一个星星⭐，这对我来说，是莫大的支持！

堪称完美的修改代码，由@befantasy提供，再次表示感谢！