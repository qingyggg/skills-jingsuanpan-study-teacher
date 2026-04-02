# jingsuanpan-study-teacher

`jingsuanpan-study-teacher` 是一个面向 `etax-go-v4` 财税项目的教学型 skill。

它把项目的代码阅读资料、项目手册、自学教材和常见缩写说明一起打包进 skill，方便：

- 新人从零开始自学项目
- 老同事快速回忆某个功能的实现链路
- 带教同学按统一方式讲业务、讲财务、讲代码
- 在没有原始 `代码阅读任务文档` 和 `项目文档` 目录的环境里继续使用

## 这个 skill 能做什么

它支持几种常见模式：

- 章节教学模式：按阶段教材一章一章讲
- 项目手册模式：按模块讲系统结构、主链路和维护要点
- 自学教材模式：适合新人循序渐进自学
- 重点精讲模式：对核心模块深讲，必要时逐行解释关键代码
- 老手速查模式：快速回忆某个功能的入口、状态、实现链路和改动风险
- 零基础新手模式：先讲业务和财务概念，再讲表结构、接口和 service

## 内置了哪些资料

这个 skill 已经把以下资料打包进 `references/`：

- `代码阅读任务文档/`
- `项目文档/`
- `表名字段缩写速查表`

这意味着：

- 即使目标项目里没有这些中文文档目录，skill 仍然能工作
- skill 会优先读内置教材，再结合当前工作区的真实代码讲解

## 适合谁用

### 1. 刚接手项目的新人

如果你只懂 Go，不懂财税业务，这个 skill 会优先：

1. 讲业务场景
2. 讲财务概念
3. 讲表结构和字段
4. 讲 `api/controller`
5. 讲重点 `service`

### 2. 已接手过项目的老同事

如果你做过这个项目，但某块功能忘了怎么实现，这个 skill 会优先给你：

- 功能归属模块
- 路由 / API / service / model 入口
- 核心状态和表
- 实现主链路
- 改动风险和下游影响

### 3. 带教和 onboarding 同学

如果你需要带新人，这个 skill 可以当项目讲义和教学助手使用。

## 项目命名风格的特殊支持

这个项目里大量表名、字段名、状态名使用拼音缩写。

为了避免新人卡在命名上，这个 skill 默认会在小白模式下主动解释：

- 缩写怎么展开
- 中文意思是什么
- 在当前模块里起什么作用

例如：

- `rzzt` -> `ren zheng zhuang tai` -> 认证状态
- `dkzt` -> `di kou zhuang tai` -> 抵扣状态
- `fphm` -> `fa piao hao ma` -> 发票号码

## 目录结构

```text
jingsuanpan-study-teacher/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── lesson-index.md
    ├── 代码阅读任务文档/
    └── 项目文档/
```

## 安装方式

把整个 `jingsuanpan-study-teacher` 目录放到：

```text
$CODEX_HOME/skills/
```

如果没有设置 `CODEX_HOME`，通常放到：

```text
~/.codex/skills/
```

## 使用示例

可以这样触发：

- “用 `jingsuanpan-study-teacher` 带我按章节学习这个项目”
- “用 `jingsuanpan-study-teacher` 按模块讲凭证中心”
- “用 `jingsuanpan-study-teacher` 重点精讲自动化工厂”
- “用 `jingsuanpan-study-teacher` 帮我快速回忆税务申报模块怎么实现”
- “用 `jingsuanpan-study-teacher` 带一个只懂 Go 的新人入门这个项目”

## 建议搭配

如果是新人持续学习，建议在项目里维护：

```text
项目文档/学习任务进度.md
```

这样多轮对话时不容易丢学习进度。

## 说明

这个 `README.md` 是为了 Git 仓库分享和团队传播补充的说明文件。

skill 本身运行主要依赖：

- `SKILL.md`
- `agents/openai.yaml`
- `references/`
