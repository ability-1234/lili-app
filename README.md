# lili-app

lili-app 是一个只使用免费服务的整合项目。本仓库用 GitHub Actions 每天定时检查 Cloudflare Worker 的公开地址是否能正常打开。

## 整合了哪些免费服务

- **Supabase**：项目名为 `lili-app`，作为本项目的后端服务。
- **Cloudflare Worker**：项目名为 `lili-hello`，公开地址为 https://lili-hello.learningask-1.workers.dev/ ，正常时应返回 `Hello from lili`。
- **Cloady**：项目名为 `lili-hello`，公开地址为 https://lili-hello-jdzo5gv5-chat-h.cloady.io/ 。
- **OpenRouter**：只使用免费模型，不使用付费模型。

## 定时检查

`.github/workflows/check-worker.yml` 每天定时（UTC 每天 00:00）请求 Cloudflare Worker 的公开地址，检查 HTTP 状态码是否为 200，并且响应内容包含 `Hello from lili`。也可以在 Actions 页面手动触发（workflow_dispatch）。

## 说明

- 本项目只做免费内容，不升级、不绑卡、不付费。
- 本仓库不存放任何密钥、Token 或密码。
