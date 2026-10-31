# utask-feed

UTaskDesktop（优学院作业助手）的在线更新物料仓库。

- `manifest.json` —— 客户端检查更新的唯一入口
- `manifests/` —— 每个已发布版本的全量文件清单（含每个文件的 SHA256）
- `patches/` —— 相邻版本之间的增量包

客户端按「本机版本 == patch.from」精确匹配一条增量包，逐文件校验 SHA256 之后替换。

**这个仓库只放分发物料，不含任何源码。**

- 单文件请勿超过 10MB（个别托管站对匿名下载有限制时会被截）
- 每次发版由 `tools\publish-update.ps1` 自动推送，手动改动请勿直接推
