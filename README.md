<h1 align="center">Grok Mirror</h1>

[![Docker](https://img.shields.io/docker/pulls/dairoot/grok-gateway?label=Grok-Mirror&logo=docker)](https://hub.docker.com/r/dairoot/grok-gateway)
[![License](https://img.shields.io/github/license/dairoot/Grok-Mirror)](./LICENSE)

Grok Mirror 后台是一个 Grok 镜像站，允许多账号共享管理。实现多人同时使用 Grok 服务。

## 特点

- 提供与官网同等的极致体验。
- 用户无需翻墙，便可轻松访问并使用 Grok 官方网站的所有功能。
- 通过在 `Mirror` 后台录入 `Sso Token`，让用户可以轻松使用 Grok 服务。

## 在线体验

https://grok.dairoot.cn

## 部署

打开命令行终端，执行以下命令

```bash
docker run --rm -p 50005:8080 \
-v grok_gateway_db:/app/.cache_data \
dairoot/grok-gateway:latest
```

访问 `http://127.0.0.1:50005` 或访问 `http://外网ip:50005`

配置域名，请点击查看[完整部署流程](./docs/deploy.md)

## 加入群聊

[Telegram](https://t.me/+34aYksZdq5ZhMzhl)

## 捐赠

[Buy Me a Coffee](https://github.com/dairoot/ChatGPT-Mirror/blob/main/docs/donation.md)

## Star History

![Star History Chart](https://api.star-history.com/svg?repos=dairoot/Grok-Mirror&type=Timeline)
