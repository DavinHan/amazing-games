# Claude 协作入口

开始任何任务前，先阅读并遵守同目录的 [AGENTS.md](AGENTS.md)，它是本仓库统一维护的协作规范。

继续阅读 [README.md](README.md) 以及目标游戏或共享包的 README；进入具体目录时，检查其中是否还有适用的局部约定。

关键约束：

- 游戏放在 `games/<game-name>/`，技术栈按游戏选择，共享代码按实际需要提取到 `packages/`。
- 默认使用中文；遵循提交规范，用中文生成 commit message，并增加 `Co-Authored-By: Codex <codex@openai.com>`。
- 当目标或计划是修改单元测试、修复单元测试问题时，禁止修改生产代码、主干代码。
- 只报告实际执行过的验证，不自动提交或推送。

新增通用约定时更新 `AGENTS.md`；本文件仅保留入口和关键约束，避免维护两份完整规范。
