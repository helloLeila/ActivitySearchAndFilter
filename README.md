# ActivitySummary

用于检索和整理粤港澳线下硬核技术活动的提示词与技能仓库。

这个仓库解决两件事：

1. 给自动化或日常检索直接使用的完整提示词。
2. 给代理调用的可复用 skill，帮助稳定筛选真实活动、输出统一格式、保留深圳候补链接。

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
