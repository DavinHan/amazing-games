# Amazing Projects · 游戏工坊

一个容纳多个独立游戏的仓库。每个游戏可以选择适合自己的语言、引擎和工具链，先把核心玩法做出来，再根据实际需要提取共享能力。

## 目录结构

```text
.
├── AGENTS.md                    # 所有 AI 编码助手的统一协作约定
├── CLAUDE.md                    # Claude 的入口，指向统一约定
├── games/                       # 独立游戏，每个游戏一个目录
│   └── <game-name>/
│       └── README.md            # 游戏说明、环境要求、运行与验证命令
├── packages/                    # 有实际复用需求后再添加共享代码
└── docs/
    └── templates/
        └── game-readme.md       # 新游戏说明模板
```

已建立 Walker 项目目录、第一阶段目标和 Windows 技术设计，尚未创建引擎工程或安装依赖。目录树中的 `<game-name>` 表示各游戏自己的目录。

## 新建一个游戏

1. 确定游戏名称、目标平台、核心玩法和第一个可玩版本的范围。
2. 在 `games/` 下创建小写短横线命名的目录，并复制说明模板：

   ```sh
   # 从仓库根目录执行；将 my-game 换成游戏名
   mkdir games/my-game
   cp docs/templates/game-readme.md games/my-game/README.md
   ```

3. 在该目录内选择并初始化工具链，填写 README 中的环境要求、运行命令和验证方式。删除模板中不适用的内容。
4. 先完成可启动、可操作、有反馈、可结束或重开的最小玩法循环，再逐步扩展。
5. 将游戏加入下方索引。

游戏的代码、素材、测试和配置默认都放在自己的目录内。素材目录、源码目录等按所选引擎的惯例组织；共享代码的使用方式见 [packages/README.md](packages/README.md)。

## 游戏索引

| 游戏 | 简介 | 技术栈 | 状态 |
| --- | --- | --- | --- |
| [Walker](games/walker/README.md) | 女性角色高跟鞋行走与第一、第三人称视角切换小样 | UE 5.8.4 / C++ + 蓝图（设计基线） | Windows 技术设计完成，待工程与资源验证 |

## 运行与验证

进入对应的 `games/<game-name>/`，按该游戏 README 执行。根目录暂时没有统一的安装、启动、构建或测试命令。

每个游戏应记录可复现的环境版本和依赖安装方式。引入包管理器后提交对应锁文件，不混用多个包管理器。

## 协作约定

开发前阅读 [AGENTS.md](AGENTS.md)。提交信息遵循 Conventional Commits，描述使用中文，例如 `feat(snake): 增加暂停和继续功能`。

每次提交附加：

```text
Co-Authored-By: Codex <codex@openai.com>
```

素材、字体、音乐、音效及第三方代码的来源和许可记录在所属游戏的 README 中。仓库尚未选定开源许可证，发布前需明确代码和素材的授权方式。
