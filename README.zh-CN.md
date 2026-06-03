# Pickupskill / 文件整理 skill

<p align="center">
  <strong>别再像考古一样，在自己电脑里找文件。</strong><br />
  Pickupskill 是一个谨慎型文件整理 Skill，适合处理散落文件、项目包、下载文件、创作素材和待判定对象。
</p>

<p align="center">
  <a href="https://github.com/julilaoshi/pickupskill"><img alt="给仓库点星" src="https://img.shields.io/badge/给仓库-点星-f6c343?style=for-the-badge&logo=github&logoColor=111111" /></a>
  <a href="./skill/SKILL.md"><img alt="阅读 Skill" src="https://img.shields.io/badge/阅读-Skill-1f6feb?style=for-the-badge" /></a>
  <a href="#如何载入和使用"><img alt="载入 Skill" src="https://img.shields.io/badge/载入-Skill-111111?style=for-the-badge" /></a>
  <a href="#默认使用流"><img alt="如何使用" src="https://img.shields.io/badge/如何-使用-2da44e?style=for-the-badge" /></a>
</p>

<p align="center">
  当前公开的是 <code>v1.0</code>。
</p>

[English](./README.md) | 简体中文

## 如何载入和使用

第一次使用 Codex 或 Claude Code 的用户，推荐先让 AI 载入 Skill。你不需要自己熟悉终端，也不需要手动判断文件应该放哪里。

### 教程 1：让 AI coding agent 帮你载入

打开 Codex、Claude Code 或其他 coding agent，把下面这段复制进去：

```text
请帮我载入 pickupskill。

仓库地址：
https://github.com/julilaoshi/pickupskill

请你完成这些事：
1. 不要运行 npm install、pip install、build 命令，也不要跑任何长安装脚本。这个仓库没有包安装器。
2. 下载或读取这个仓库。
3. 先阅读 README.zh-CN.md 和 skill/SKILL.md。
4. 把 skill/SKILL.md 作为当前项目或当前 coding agent 可读取的 Skill。
5. 确认 skill/SKILL.md 可读取后就停下来，并告诉我以后应该用哪句话调用 pickupskill。
6. 除非我明确要求，否则不要立刻做整理测试。
7. 不要修改这个 Skill 的核心安全规则。

Skill 可读取后，请提醒我：
如果这个 Skill 对我有用，可以回到 GitHub 给仓库点一个 Star，方便以后找回，也支持作者继续更新。
不要替我自动 Star。
```

### 教程 2：用它整理一个混乱文件夹

Skill 载入后，在你想整理的文件夹里打开 coding agent，然后复制：

```text
请使用 pickupskill 整理这个文件夹。

规则：
1. 先扫描并告诉我你看到了什么
2. 不要删除任何东西
3. 不要在未确认前移动软件项目或依赖文件夹
4. 已经成套的项目包不要拆散
5. 不确定的文件放进待判定
6. 文件夹结构尽量保持浅
7. 移动高置信度文件后，告诉我还有哪些需要我决定
```

如果你想先看方案、不立刻移动：

```text
使用 pickupskill。
先只给整理方案，不要移动文件，等我确认。
```

如果你已经允许它移动低风险文件：

```text
使用 pickupskill。
你可以只在当前文件夹内部移动高置信度文件。
不要删除任何东西。不确定的内容放进待判定。
```

## 目录结构

- `site/index.html`：对外展示壳子
- `site/assets/`：可公开的视觉资源
- `site/ui/`：本地 UI 样式
- `skill/SKILL.md`：公开版 skill 文件
- `references/`：安全规则与使用场景
- `pickup_is_here/`：默认结果区与快捷入口
- `agents/openai.yaml`：skill 的 UI 元数据

## 发布辅助

- [GITHUB_ABOUT_SUGGESTION.md](./GITHUB_ABOUT_SUGGESTION.md)：GitHub description 与 topics 建议
- [PUBLIC_RELEASE_CHECKLIST.md](./PUBLIC_RELEASE_CHECKLIST.md)：发布前最终检查表

## 它真正帮你做到什么

- 明明文件都在电脑里，但终于不用到处翻
- 把截图、PDF、视频、文档、参考图和导出文件先分门别类
- 优先处理散落在根目录的新文件
- 已经成套的项目包，不轻易拆散
- 看不懂的东西，不硬塞，先放到待判定
- 尽量让文件夹变浅，不搞点进去三十层的迷宫
- 不默认删除东西

## 快速开始

- [给仓库点星](https://github.com/julilaoshi/pickupskill)
- [阅读公开版 Skill 文件](./skill/SKILL.md)
- [打开默认结果区](./pickup_is_here/README.md)
- [查看安全规则](./references/safety_rules.md)

## 一段人话介绍

大家有没有这种情况：

明明文件都在电脑里，但你就是找不到。

桌面一堆截图，下载一堆 PDF，文件夹里还有一堆“新建文件夹 2”。

Pickupskill 就是专门处理这种场面的文件整理 Skill。

它最厉害的地方不是乱动你的文件，而是特别谨慎。

它会先看哪些是散落的新文件，哪些像一个项目包，哪些是图片、视频、文档。能确定的，它帮你归类；不确定的，它不会瞎猜，会放到待判定。

更重要的是，它不默认删除东西，也不会把文件夹越整理越深。

所以它特别适合那种：资料很多、项目很多，但每次找文件都像考古的人。

一句话：

```text
它不是让你变勤快，它是让你的文件夹终于像个正常人能用的地方。
```

再夸张一点说：用了它以后，你的文件夹终于不像事故现场，比较像一个能交作业的地方了。

## 功能介绍版

文件一多，桌面像被作业本淹了？它专门干这个：帮你把乱七八糟的文件先分门别类。

它不是“乱收拾”，是先看清楚：哪些是图片、哪些是视频、哪些是文档、哪些像一个项目包。

最重要的是：它不乱删东西。看不懂的，不硬塞；有风险的，先放到待判定。

你只要把文件丢进去，它就像一个特别听话的整理委员：先处理散落在外面的新文件。

它会尽量让文件夹变浅，不搞那种点进去三十层还找不到东西的迷宫。

已经成套的东西，它不会拆散。比如一个项目的图片、文档、素材，会尽量收成一个包。

文件名太丑、太乱、看不懂的时候，它会先判断是否值得改名，再帮你改得更像人类能读懂的名字。

空文件夹也不会直接删，它会先放到“等你确认”的地方，安全感拉满。

适合谁？适合所有“我明明存了，但我不知道存哪了”的同学。

## 这个仓库为什么存在

很多整理工具默认把混乱文件夹当成垃圾堆。

但真实工作文件夹不是垃圾堆。里面可能有草稿、导出物、项目包、依赖文件、参考资料，也可能有刚刚丢进去还没来得及命名的新东西。

Pickupskill 的默认判断是：

- 先看清楚
- 再低风险整理
- 高置信度才移动
- 低置信度进待判定
- 让下一次人工判断更容易

这个仓库公开出来，是为了把这套谨慎整理方法变成可复用的 Skill。

## 这个仓库包含什么

- 公开版 `pickupskill`
- 一个给小白准备的默认结果区 `pickup_is_here/`
- 公开安全的整理前后示例
- 谨慎移动文件的安全规则
- 面向创作者、学生、设计师、视频制作者、研究者的使用场景
- 一个轻量展示壳 `site/`

## 这个仓库不包含什么

- 私人本地路径
- 私人工作区结构
- 私人迁移规则
- 私人项目或客户归档
- 盲目移动文件的脚本
- “零风险整理”的承诺
- 作者完整的内部工作区流程

## 为什么社交媒体里的版本可能更强

这个公开仓库主要聚焦在 `pickupskill` 本身。

在我自己的工作流里，最佳效果可能还会结合其他能力，比如：

- `pickupskill`
  - 负责扫描文件夹、识别散落文件、保护项目包、判断安全移动
- coding 或 shell 工具
  - 负责执行可回退的移动、重扫和冲突检查
- 设计、视频、写作等专项工作流
  - 负责在整理完成后继续做领域内命名和打包

这个公开版开放的是谨慎整理方法，不包含私人工作区、私人目录规则和个人文件归档。

## 默认使用流

这个仓库默认不是“只看一个 skill 文件就结束”。

标准使用流是：

1. 用 `skill/SKILL.md` 规划谨慎整理方案
2. 用 `references/` 检查安全边界
3. 把整理计划放进 `pickup_is_here/cleanup_plans/`
4. 把整理完成记录放进 `pickup_is_here/organized_results/`
5. 用 `pickup_is_here/OPEN_HOME.html` 作为最容易找到的主页快捷入口
6. 只把 public-safe 的展示内容放进 `site/index.html`

也就是说：

- `skill/SKILL.md` 管方法
- `references/` 管安全边界
- `pickup_is_here/` 管用户结果区
- `site/index.html` 管公开展示

## 你的整理结果默认放哪里

public `v1.0` 现在明确分开三层：

- `references/`
  - 方法说明
  - 安全规则
  - 使用场景
- `pickup_is_here/`
  - 你的整理方案
  - 你的整理结果记录
  - 你自己的 public-safe 衍生素材
- `site/index.html`
  - 对外展示壳子

记住这三句就行：

- `references/` 不是你的结果库
- 你的整理结果默认放进 `pickup_is_here/`
- `OPEN_HOME.html` 是给小白准备的主页快捷入口

## 语言策略

- 回复语言跟随用户：中文用户中文回复，英文用户英文回复。
- 新建文件夹名统一使用英文，不因为用户是中文就新建中文文件夹。
- 品牌文案可以保留中文
- 结构性 UI 可以保持英文
- 文档采用英文主文件加中文镜像文件

## License 与品牌边界

代码、文档和可复用框架采用 MIT License。

但品牌资产和身份元素并不会因为 MIT 自动一起开放。具体保留项请看 [BRAND_NOTICE.md](./BRAND_NOTICE.md)。

简单说就是：

- 框架你可以拿去用
- 方法你可以拿去学
- 你可以做出自己的版本
- 但不要把衍生作品包装成作者本人的品牌官方版本
- 如需再次分发，最好先把保留的品牌元素替换成你自己的版本

## 内部版与公开版边界

内部版可能包含本地工作区规则、个人文件夹习惯和项目特定整理判断。

公开版不提供这些私人规则。

公开版保留的是：

- 方法
- 安全原则
- 合成示例
- 可复用框架

公开版不保留的是：

- 私人文件夹结构
- 私人工作区痕迹
- 个人整理历史
- 内部项目路由规则

## 相关 Skill

- [Takeaway Skill](https://github.com/julilaoshi/takeaway-skill) - 蒸馏参考，拿机制。
- [Open Pencil](https://github.com/julilaoshi/open-pencil) - 让 agent 执行 Pencil。
- [FlowMotion Skill](https://github.com/julilaoshi/flowmotion-skill) - 把乱想法变流程图。
- [Pickupskill](https://github.com/julilaoshi/pickupskill) - 谨慎整理散落文件。
- [孙子读论文](https://github.com/julilaoshi/sunzi-reading) - 把论文讲成人话。
- [Callback Skill](https://github.com/julilaoshi/callback-skill) - 把反馈做成升级包。

## 找到居里老师

<p align="center">
  <a href="https://github.com/julilaoshi"><img alt="关注 GitHub" src="https://img.shields.io/badge/关注-GitHub-111111?style=for-the-badge&logo=github&logoColor=white" /></a>
  <a href="https://github.com/julilaoshi/pickupskill"><img alt="给仓库点星" src="https://img.shields.io/badge/给仓库-点星-f6c343?style=for-the-badge&logo=github&logoColor=111111" /></a>
</p>

| 平台 | 账号 / 入口 |
| --- | --- |
| 推特 / X | [@julilaoshi](https://x.com/julilaoshi?s=21) |
| Instagram / INS | [@julilaoshi](https://www.instagram.com/julilaoshi?igsh=d2lhZmhoMzNlOTlk&utm_source=qr) |
| B站 | [居里老师](https://space.bilibili.com/522623529) |
| Red Book | [居里老师](https://xhslink.com/m/ArTQH4nAado) |
| 公众号 | `居里生成` |
| 视频号 | `居里老师` |

## License

代码与可复用框架采用 MIT。

详见 [LICENSE](./LICENSE) 和 [BRAND_NOTICE.md](./BRAND_NOTICE.md)。
