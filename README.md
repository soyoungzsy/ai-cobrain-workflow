# AI 共脑工作流

作者 <span class="notranslate" translate="no">Soya</span>

> 把无限增长的 Todo 清单，变成一套人机协作闭环。

AI 共脑工作流面向同时处理多个项目的知识工作者。它帮助 AI 回答普通待办清单没有解决的三个问题：

1. **下一棒轮到我、AI，还是协作者？**
2. **这件事现在应该出现，还是等日期或依赖变化后再出现？**
3. **需要什么证据，才能判定它真正完成？**

本仓库只包含通用方法、Prompt、模板和完全虚构的示例，不连接任何企业系统，不含真实工作数据，也不宣称对所有用户都已经产生确定的效率提升。

[English](README.en.md) · [安装Skill](skills/ai-cobrain/SKILL.md) · [5分钟上手](docs/quickstart.md) · [备用Prompt](prompts/cobrain-secretary.md) · [隐私与安全](docs/privacy-and-security.md)

## 直接安装 Skill

仓库的核心资产是 [`ai-cobrain`](skills/ai-cobrain/SKILL.md) Skill。它不依赖公司插件、私有系统或特定任务软件。

### Codex

```bash
git clone https://github.com/soyoungzsy/ai-cobrain-workflow.git
mkdir -p ~/.codex/skills
cp -R ai-cobrain-workflow/skills/ai-cobrain ~/.codex/skills/
```

### Claude Code

```bash
git clone https://github.com/soyoungzsy/ai-cobrain-workflow.git
mkdir -p ~/.claude/skills
cp -R ai-cobrain-workflow/skills/ai-cobrain ~/.claude/skills/
```

安装后重新打开客户端，然后直接说：

```text
用 $ai-cobrain 整理下面这些事项，给出今天三个关键结果，
并直接完成 AI 可以处理的部分。
```

没有安装条件时，再使用仓库中的[备用Prompt](prompts/cobrain-secretary.md)。

## 为什么普通 Todo 不够

- 所有未完成事项每天重复出现，持续占用注意力；
- “已通知、已审批、已配置”容易被误认为真正完成；
- 多人协作时，下一步究竟轮到谁并不清楚；
- 等待日期或外部依赖的事项，没有新的变化也会反复提醒；
- AI 生成了更多内容，却没有真正分担协调压力。

AI 共脑工作流把任务看作一个**持续变化的交接状态**，而非一个静态复选框。

## 六步闭环

`收集信号 → 判断重点 → 分配下一棒 → 等待条件 → 验收结果 → 写回学习`

| 机制 | 解决的问题 |
| --- | --- |
| 每天最多三个关键结果 | 待办堆积冒充今日计划 |
| 每项只有一个当前下一棒 | 多人都关注，但没人真正推进 |
| 按触发条件重新出现 | 未来事项过早消耗今天的注意力 |
| 独立完成标准 | 过早划掉任务 |
| 人工确认门 | AI猜测Owner、时间和高风险决策 |
| 每日校准规则 | Prompt长期不理解你的判断习惯 |

## 不安装 Skill 的备用方式

1. 把 [`prompts/cobrain-secretary.md`](prompts/cobrain-secretary.md) 整段复制给你的 AI；
2. 只粘贴最近一至三天、一个项目范围内的脱敏任务；
3. 人工纠正优先级、下一棒、再次出现条件和完成标准；
4. 用 [`templates/daily-workbench.md`](templates/daily-workbench.md) 保存当天结果；
5. 收工时告诉 AI：它今天排错了什么、哪件事划早了、哪些规则值得保留。

第一天不要追求全自动，也不要一次接入所有聊天、邮件和日历。

## 与常见 Personal OS 的区别

本项目不试图管理生活的所有方面，也不预设复杂的多智能体架构。它只聚焦一个窄而高频的问题：**如何让 AI 真正分担并发任务的协调成本，同时保留人的判断和责任。**

核心差异是三个字段：`next_actor`、`wake_trigger`、`acceptance_criteria`。

## 管理者与下属协作场景

“协作者”可以是下属、项目搭档、跨团队同学或外部合作方。管理者可以让 AI 根据共同目标，为下属生成当天可执行的 Todo 清单，并写清：

- 今天需要推动什么结果；
- 每项任务的具体下一步；
- 需要返回什么证据或回执；
- 当前依赖和异常升级条件；
- 哪些事项尚未到节点，不应反复催办。

AI 负责整理和降噪，正式优先级、责任人和任务布置仍由管理者确认。这套方法不用于监控员工，也不能根据消息数量、响应速度或任务元数据推断个人态度和绩效。

## 项目成熟度

`v0.2.0` 已提供可安装 Skill、Prompt、任务模型与模板。方法来自真实工作实践，但公开版本还没有经过大量独立用户验证。请把它视为可试跑的起点，不要把它当作普适生产力结论。

## 许可证

MIT，详见 [LICENSE](LICENSE)。

## 来源与证据

- 项目方法来自 <span class="notranslate" translate="no">Soya</span> 日常人机协作工作流的脱敏抽象。
- 同类项目核对仅用于明确公开定位，没有复制其文档、代码或私有材料。

## 修改记录

- 2026-09-19：创建可公开的中文首版说明。
- 2026-09-20：增加可直接安装的`ai-cobrain` Skill，并将Prompt调整为备用入口。
