# SakuraMedia API 文档

上游 `tinypinglite/sakuramediabe` v0.9.8（main `5684ffe`）的完整接口文档，用于后端 Rust 重构测试对照。

- **在线浏览**：https://zxsos.github.io/sakuramedia-api-docs/
- **OpenAPI 规范**：[sakuramedia-openapi.yaml](./sakuramedia-openapi.yaml)（OpenAPI 3.1.0）

## 内容概览

| 项目 | 数量 |
|---|---|
| 接口总数 | 186（143 个 path） |
| 数据模型 | 245 |
| 功能域 | 8（catalog / collections / discovery / files / playback / system / transfers / videos） |

## 说明

- 每个接口含中文说明、请求/响应模型、预期结果及前端（Flutter）调用对照
- 鉴权：`Authorization: Bearer`（JWT 或 `sk-` 前缀 API Key）；7 个公开接口无需鉴权
- 分页统一 `PageResponse` 结构，错误统一 `{"error": {"code","message","details"}}` 格式
- 文档由后端路由静态分析 + 前端调用映射自动生成，生成脚本见 `~/workspace/upstream/gen_openapi.py`

## 相关仓库

- 后端上游：https://github.com/tinypinglite/sakuramediabe
- 前端上游：https://github.com/tinypinglite/sakuramedia
- Rust 重构：https://github.com/zxsos/sakuramediabe-rs
