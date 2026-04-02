# Lesson Index

Use this index as the navigation layer for teaching the 鲸算盘 `etax-go-v4` project.

## Bundled Reference Root

- `references/`

These references are bundled inside the skill so the teaching workflow still works even if the target repository does not contain `代码阅读任务文档/` or `项目文档/`.

## Core Curriculum

- Integrated handbook:
  - `references/项目文档/鲸算盘财税系统功能模块与项目手册.md`

- Self-study textbook:
  - `references/项目文档/鲸算盘财税系统自学教材.md`

- Curriculum overview:
  - `references/代码阅读任务文档/代码阅读任务表.md`

- Chapter 3:
  - `references/代码阅读任务文档/第3阶段-企业与账套管理教材.md`

- Chapter 4:
  - `references/代码阅读任务文档/第4阶段-建账与会计基础数据教材.md`

- Chapter 5:
  - `references/代码阅读任务文档/第5阶段-凭证与会计主流程教材.md`

- Chapter 6:
  - `references/代码阅读任务文档/第6阶段-发票银行工资三大单据源教材.md`

- Chapter 7:
  - `references/代码阅读任务文档/第7阶段-结转结账报表账簿教材.md`

- Chapter 8:
  - `references/代码阅读任务文档/第8阶段-税务申报任务系统教材.md`

- Chapter 9:
  - `references/代码阅读任务文档/第9阶段-自动化工厂教材.md`

- Chapter 10:
  - `references/代码阅读任务文档/第10阶段-代码级维护能力教材.md`

## Supporting Notes

Open these only when the current lesson needs lower-level factual grounding:

- `references/代码阅读任务文档/代码解析/企业账套.md`
- `references/代码阅读任务文档/代码解析/建账初始化.md`
- `references/代码阅读任务文档/代码解析/发票.md`
- `references/代码阅读任务文档/代码解析/银行流水.md`
- `references/代码阅读任务文档/代码解析/员工薪酬.md`
- `references/代码阅读任务文档/代码解析/结转与结账.md`
- `references/代码阅读任务文档/代码解析/财务报表.md`
- `references/代码阅读任务文档/代码解析/账薄查询.md`
- `references/代码阅读任务文档/代码解析/税务申报模块.md`
- `references/代码阅读任务文档/代码解析/自动化记账.md`
- `references/代码阅读任务文档/代码解析/个人企业财税.md`

## Teaching Modes

- Chapter mode:
  - Start from the staged lesson files in `references/代码阅读任务文档/`
  - Use when the user asks for chapter-by-chapter teaching or says “继续下一章”

- Handbook mode:
  - Start from the integrated handbook in `references/项目文档/鲸算盘财税系统功能模块与项目手册.md`
  - Use when the user wants a structured system overview, module classification, or maintenance map

- Self-study mode:
  - Start from `references/项目文档/鲸算盘财税系统自学教材.md`
  - Use when the user wants material suitable for self-learning, onboarding, or internal training

- Deep-dive mode:
  - Start from the handbook/self-study text, then inspect code files
  - Use when the user asks for “重点讲”, “精讲”, “逐行解释”, or deep code walkthroughs

- Quick-reference mode:
  - Start from `references/项目文档/鲸算盘财税系统功能模块与项目手册.md`
  - Then inspect the current workspace code for route/API/service/model entry points
  - Use when the user already knows the project and wants implementation recall, maintenance lookup, or risk review

- Zero-basics mode:
  - Start from `references/项目文档/鲸算盘财税系统自学教材.md`
  - Begin with business and finance concepts before code
  - Use when the user says they only know Go, are new to finance, or need true beginner onboarding

## Core Modules For Deep Teaching

- Enterprise, company, account-set, and period context
- Initialization and book creation
- Voucher center
- Invoice, bank, salary
- Carryover and checkout
- Tax task system
- Automation factory

For these modules, prioritize:

- business meaning
- finance meaning
- key route/API/service/model files
- state fields and status transitions
- key code blocks and important branches

## Teaching Defaults

- Default to Chinese.
- Teach one chapter at a time.
- Start with business meaning, then finance meaning when relevant, then code entry points, then key takeaways.
- If the user says “继续”, move to the next chapter in numeric order.
- If the user asks for a code deep dive, open the relevant handbook/chapter first, then inspect the relevant repository files.

## Output Shapes

- For experienced users:
  - prefer recall-oriented answers
  - list route/API/service/model quickly
  - emphasize state fields, data tables, and modification risk

- For zero-basics users:
  - define terms like 企业, 账套, 账期, 凭证, 结账, 税表 before using them heavily
  - explain one main concept at a time
  - map each concept to 1-3 concrete files in the repository
