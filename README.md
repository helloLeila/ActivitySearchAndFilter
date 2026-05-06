# ActivitySummary

用于检索和整理粤港澳线下硬核技术活动的提示词与技能仓库。

这份 skill 按“多平台通用”设计，目标平台包括：

1. Claude Code
2. Codex
3. 其他具备网页检索能力的代理

这个仓库解决两件事：

1. 给自动化或日常检索直接使用的完整提示词。
2. 给代理调用的可复用 skill，帮助稳定筛选真实活动、输出统一格式、保留深圳候补链接。

## 为什么之前 Claude Code 会跑很久

你原来的提示词判断力很强，但也有一个副作用：

1. 来源清单很长
2. “必须优先检索这些来源”这句话执行感很强
3. 之前没有明确写“找到足够结果就停”
4. 也没有明确写“不要把来源池当成穷举清单”

Claude Code 比较容易把这类提示词执行成“继续搜，直到证明自己真的搜得很全”，所以会出现长时间检索。

现在仓库里已经补了：

1. 分阶段检索
2. 检索预算
3. 停机条件
4. 跨平台兼容说明

## 仓库结构

- `prompts/activity-summary-prompt.md`
  - 可直接复制到自动化、定时任务或手动检索中的完整提示词
- `skills/activity-summary/SKILL.md`
  - 技能主文件，定义什么时候触发、怎么检索、怎么筛选、怎么输出
- `skills/activity-summary/agents/openai.yaml`
  - 技能展示元数据
- `skills/activity-summary/references/output-template.md`
  - 固定输出模板
- `skills/activity-summary/references/source-checklist.md`
  - 优先信息源与检索顺序
- `skills/activity-summary/references/filtering-rubric.md`
  - 收录、排除、候补与排序规则

## 适用场景

- 每日或每周检索深圳、广州、珠海、香港、澳门的真实技术活动
- 需要同时兼顾“真实性”和“可读性”的活动简报
- 需要把英文活动补成更友好的中文解释
- 需要在主清单为空时附带深圳候补链接

## 当前状态

仓库内容已本地创建并初始化为 git 仓库。

当前环境未安装 `gh`，所以还没有直接推送到 GitHub 远端。等安装或配置 GitHub CLI 后，可以继续完成：

1. 创建 GitHub 仓库
2. 首次 commit
3. push 到远端
