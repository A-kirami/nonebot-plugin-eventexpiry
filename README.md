<div align="center">
  <a href="https://v2.nonebot.dev/store"><img src="https://github.com/A-kirami/nonebot-plugin-template/blob/resources/nbp_logo.png" width="180" height="180" alt="NoneBotPluginLogo"></a>
  <br>
  <p><img src="https://github.com/A-kirami/nonebot-plugin-template/blob/resources/NoneBotPlugin.svg" width="240" alt="NoneBotPluginText"></p>
</div>

<div align="center">

# nonebot-plugin-eventexpiry

_✨ 自动过滤过期事件 ✨_


<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/A-kirami/nonebot-plugin-eventexpiry.svg" alt="license">
</a>
<a href="https://pypi.python.org/pypi/nonebot-plugin-eventexpiry">
    <img src="https://img.shields.io/pypi/v/nonebot-plugin-eventexpiry.svg" alt="pypi">
</a>
<img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="python">

</div>

## 📖 介绍

检查每个事件的产生时间，如果超过指定的过期时间，那么这个事件会被忽略。

可能的应用场景：

go-cqhttp 在未连接时会将所有事件积压，待连接建立后全部上报，而这些事件可能已经过时，你可以使用本插件来清理这些事件。

## 💿 安装

<details open>
<summary>使用 nb-cli 安装</summary>
在 nonebot2 项目的根目录下打开命令行, 输入以下指令即可安装

    nb plugin install nonebot-plugin-eventexpiry

</details>

<details>
<summary>使用包管理器安装</summary>
在 nonebot2 项目的插件目录下, 打开命令行, 根据你使用的包管理器, 输入相应的安装命令

<details>
<summary>pip</summary>

    pip install nonebot-plugin-eventexpiry
</details>
<details>
<summary>pdm</summary>

    pdm add nonebot-plugin-eventexpiry
</details>
<details>
<summary>poetry</summary>

    poetry add nonebot-plugin-eventexpiry
</details>
<details>
<summary>conda</summary>

    conda install nonebot-plugin-eventexpiry
</details>

打开 nonebot2 项目根目录下的 `pyproject.toml` 文件, 在 `[tool.nonebot]` 部分追加写入

    plugins = ["nonebot_plugin_eventexpiry"]

</details>

## ⚙️ 配置

在 nonebot2 项目的`.env`文件中添加下表中的必填配置

| 配置项 | 必填 | 默认值 | 说明 |
|:-----:|:----:|:----:|:----:|
| EVENTEXPIRY_EXPIRE | 否 | 30 | 指示插件应忽略多少秒前的事件，默认30秒 |
