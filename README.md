# 物理题库（线上站点产物）

个人物理题库：上传试卷 → 自动解析切割 → 智能标注 → 检索组卷 → 导出打印。

本仓库只存放**构建后的静态产物**（GitHub Pages 托管用），源码在本地开发仓库中维护。

- 站点地址：https://lqlxhwjm1129-ops.github.io/physics-tiku/
- 构建版本：见 `index.html` 内注入的版本号，或应用内「设置」页顶部显示
- 后端：WorkBuddy 云服务（数据库 / 登录 / 文件存储），跨域已放行

## 更新流程

1. 本地执行 `npm run release -- --note "改动说明"` 生成新版本产物
2. 把 `dist/` 内容同步到本仓库根目录，并补上 `404.html`（内容同 `index.html`，用于前端路由深链兜底）
3. 提交并推送到 `main` 分支，GitHub Pages 会自动重新部署
