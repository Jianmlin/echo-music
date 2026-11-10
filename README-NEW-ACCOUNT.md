Echo Music 0.19.0 — 新账号代码备份

目标 GitHub 账号：Jianmlin

本安装包只保存代码、图片、字体、示例音频和安装说明，不包含旧账号的用户数据库、密码、会话或部署密钥。

文件：
1. echo-music-source.zip：完整源码，含网站前端、Apps Script、头像及音乐服务函数、测试、GitHub Pages 工作流。
2. apps-script-setup.zip：完整 Code.gs、Config.gs、manifest、邮件模板与依赖许可证。
3. SHA256SUMS.txt：两个子安装包的校验值。

这是源码保存，不代表新账号的网站或后端已经部署。

之后重新接入：
- 将完整源码解压后放到 Jianmlin 的新 GitHub 仓库。保留图片、字体、音频等二进制文件。
- 使用新 Google 账号创建私有管理表和 Apps Script 项目。原 Config.gs 和网页配置中的旧表 ID、后端地址需要替换。
- 前端配置在 dist/config.js；构建脚本为 scripts/write-config.mjs。
- 邮件中的网站及 Logo 地址、Safari 脚本的网站匹配地址，也需要改成新站点地址。
- 头像、广场图片及音乐搜索仍需要配置相应服务；对应 Supabase 函数和迁移代码保存在 supabase/。
- 新库为空；管理员引导和首次启用需要按新环境设置，不要直接执行文档中针对旧数据的迁移或旧项目升级步骤。
- 邮件密钥、密码加密 pepper 等运行密钥只放在新项目的私有属性中，不放到 GitHub。

旧项目 README 保留用于代码历史说明，不能代替新账号的部署配置。
