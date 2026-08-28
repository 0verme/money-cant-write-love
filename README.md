# money-cant-write-love

> **钱可以买到很多东西。**<br>
> **但钱写不出爱。**

**Money can buy almost everything. A writing skill for the things it can't.**

![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827) ![Claude Code](https://img.shields.io/badge/Claude_Code-Compatible-D97757) ![License](https://img.shields.io/badge/License-MIT-3DA639)

一个面向 Codex / Claude Code 的中文写作 Skill。它围绕一条主线：**财富解决表层事件，故事发生在财富失效的位置。**

一个能订机票、订酒店、找律师、调医生、雇司机、改所有人日程的人，仍然可能无法亲自出现、无法说一句"不"、无法相信一个人、无法陪另一个人等待。这中间的空缺，就是这个 Skill 写作的全部对象。

**你可以用它：**

- 把一段经历写成克制、具体、没有廉价的"难过"的第一人称短篇。
- 把普通故事改造成"资源充足但关系缺席"的叙事。
- 审稿、压缩、去 AI 味，用同一套模型打分并给出删 / 留 / 补 / 换。

---

## 这个 Skill 会把故事写成什么样

普通写法：

> 我很忙，最后她离开了我，我很难过。

使用这个 Skill：

> 律师来了三次。每一次，她都坐在客厅那张椅子里，面前放着一杯没动过的水。
>
> 三次我都在开会。会议是助理排的，为了排进去，取消了另外七个参会人的日程。
>
> 合同翻到第三页，她问：你能不能自己来一次。
>
> 我说：明天让司机去接你。
>
> 她说：不用了。
>
> 退房那天，酒店打电话来，说房间里有一件外套。外套是她的，洗衣单显示最后一次熨烫在两个月前。
>
> 我让助理寄回去。助理问她要收件地址，她说：不用了。
>
> 那间房的月租还在扣。我让财务留着。

这里发生了什么：

- **数字**建立了代价：三次、七个日程、两个月。
- **劳动**可见：助理排会、司机接送、酒店洗衣、财务扣费——所有事都有人完成。
- **缺席**可见：一杯没动过的水，一件没人来取的外套。
- **Unbuyable Gap** 显形：她只提了一个要求——"你自己来一次"——而他用司机回答。
- **系统仍在执行**：关系已经停止，月租还在扣。

全文没有一个"难过"，读者自己完成了判断。

---

## What / Why

**What**：一个三层模型的写作方法——`Reader State → Unbuyable Gap → Evidence`。

**Why**：大部分"克制写作"要求你少写、写具体、别煽情。但"少写"是结果，不是方法。这篇 Skill 回答的是"少写什么、多写什么、凭什么读者会自己感受"：

- 写作前先问读者在哪里（Reader State），而不是作者想说什么。
- 故事必须有一个钱解决不了的缺口（Unbuyable Gap），否则资源只是布景。
- 情绪一律用证据交付（Evidence），不用情绪词。

## Reader State

写作的每一步都围绕读者此刻的四个状态：

```text
K = Knowledge  读者现在知道什么？
J = Judgment   读者现在如何判断人物？
E = Expectation 读者期待接下来发生什么？
T = Tension    当前情绪张力应该增加还是释放？
```

**每一条重要信息，至少改变一个 Reader State。** 如果一个细节不改变任何状态，删除它。

## Unbuyable Gap

本项目的核心概念。每篇故事选定**一个**资源无法解决的缺口：

- 亲自出现
- 承担责任
- 相信一个人
- 说一句"不"
- 承认恐惧
- 接受失控
- 陪另一个人等待
- 做一个无法委托的决定

> 财富解决表层事件。故事发生在财富失效的位置。
>
> 一个习惯让系统解决问题的人，最终遇到了一个只能由本人完成的问题。

## Evidence

不写 Emotion，写 Evidence。六类证据账本：

| 账本 | 内容 | 举例 |
| --- | --- | --- |
| Numbers | 金额、时间、重量、次数、距离 | 取消七个日程 |
| Objects | 照片、钥匙、票据、提醒、外套 | 一杯没动过的水 |
| Labor | 司机、助理、保洁、律师、财务 | 洗衣单盖的章 |
| Space | 空房间、空座位、没人住的酒店房 | 客厅那张椅子 |
| Transactions | 账单、合同、押金、订阅、赔偿 | 还在扣的月租 |
| Actions | 删除→恢复、打开→没发送、付款→停顿 | 他说：让司机去接你 |

规则：每个昂贵细节必须承担实际叙事功能；核心物件至少出现两次，再次出现含义必须改变。

## Narrative Engine

默认八场景引擎，骨架是"模式建立 → 模式失效 → 系统残余"：

```text
Scale → Relationship → Pattern → System → Unbuyable Request
→ Pattern Break → Aftermath → Return
```

- `Scale`：建立两个具体尺度。
- `Relationship`：用小动作 / 物件建立关系。
- `Pattern`：建立"资源总能解决问题"的重复模式。
- `System`：展示服务系统如何执行。
- `Unbuyable Request`：出现不能付款解决的请求。
- `Pattern Break`：原模式第一次失效。
- `Aftermath`：人走了，合同、提醒、保洁、账单继续。
- `Return`：回收数字 / 物件 / 动作 / 空间，含义已变。

## Write / Review

**Write Mode**：把经历写成故事。Agent 内部依次完成 Reader State → Unbuyable Gap → Narrator Gap → Evidence 六账本 → Scene Plan → Information Release → Ending Return，然后**只输出标题 + 正文**，不暴露内部分析表。

**Review Mode**：审稿、压缩、去 AI 味。按十维 100 分量表（见 `references/review-rubric.md`）输出：一句话结论、最强三处、Reader State、Unbuyable Gap、Narrator Gap、技巧重复、事实可信度、删 / 留 / 补 / 换。禁止只说"很高级""很有感觉"。

## Installation

安装前请确认当前 Agent Skills 的加载规则；以下为常见配置。

### Codex

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/0verme/money-cant-write-love.git \
  ~/.codex/skills/money-cant-write-love
```

下一轮对话即可调用：

```text
使用 $money-cant-write-love，把下面这段经历写成一篇克制的第一人称故事。
```

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/0verme/money-cant-write-love.git \
  ~/.claude/skills/money-cant-write-love
```

直接调用：

```text
/money-cant-write-love 帮我把下面的经历写成一个故事。
```

也可以安装为项目 Skill 随仓库共享（`.claude/skills/money-cant-write-love`）。若该目录是在 Claude Code 启动之后才创建的，需要重启一次会话才能被识别。

## 使用方法

安装完成后，直接用自然语言调用。Skill 会自动判断你是在写还是在审。

### Write Mode —— 写

```text
使用 $money-cant-write-love，把下面这段经历写成一篇克制的第一人称故事。
```

可以附加参数控制输出：

```text
字数：800 字以内
视角：第一人称
核心缺口：亲自出现
结尾：回收那把椅子
```

Skill 会在内部依次完成 Reader State → Unbuyable Gap → Narrator Gap → Evidence 六账本 → Scene Plan → Ending Return，然后**只输出标题 + 正文**，不会把内部表格摊给你看。

触发词：钱写不出爱、克制、冷一点、不要煽情、写故事 / 写经历 / 写回忆、去 AI 味。

### Review Mode —— 审

```text
使用 $money-cant-write-love 审查下面这篇文章，并给出修改建议。
```

输出固定为九步：一句话结论（含总分）→ 最强三处 → Reader State → Unbuyable Gap → Narrator Gap → 技巧重复 → 事实可信度 → 删 / 留 / 补 / 换 →（你要求时）重写稿。

触发词：审稿、找问题、压缩、改稿、诊断、打分、太煽情。

## 使用样例

### 写

你提供：

```text
使用 $money-cant-write-love，把这段经历写成一篇 800 字以内的第一人称故事：
父亲去世后，我每月汇款让老家的表姐照看奶奶，自己从不回去。
```

Skill 输出：

```text
《汇款》

表姐每月发一张照片过来。角度一样，椅子一样，奶奶的样子也一样。

医药费从六千涨到九千的时候，表姐说：你要不要自己回来看看。
我说：钱已经转过去了。
她说：不是钱的事。

后来照片停了。最后一条消息是：下个月不用汇了。
我查了一下，那个月的转账还是按时转了出去。
```

数字、劳动、物件、账单各占一格，没有一个情绪词。缺口是"亲自出现"，结尾是系统继续执行。

### 审

你提供：

```text
使用 $money-cant-write-love 审一下这篇稿子：
（粘贴正文）
```

Skill 输出开头：

```text
一句话结论：机制成立，但中段三个场景重复了同一套"数字 + 劳动 + 冷句"（82/100）。

最强三处：……
```

如果你要求重写，它会先列出改写原则，再给新稿。

## File Structure

```text
money-cant-write-love/
├── README.md
├── SKILL.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    ├── writing-principles.md
    └── review-rubric.md
```

渐进加载：`SKILL.md` 负责执行与路由；`references/writing-principles.md` 只有深入打磨时才读取；`references/review-rubric.md` 在审稿时读取。参考资料不占每次调用的上下文。

## Inspiration & Attribution

本项目受两个开源项目启发，在此明确致谢：

- **[orange2ai/new-concept-writing](https://github.com/orange2ai/new-concept-writing)** —— 启发了 **Reader State**（读者认知状态作为上层控制模型）、**克制叙事**（零解释、物件代替心理）、**信息差**（读者知道的比叙述者说出来的多）与**减法**（删稿、禁用语）。
- **[AAAAAAAJ/sun-yuchen-writing](https://github.com/AAAAAAAJ/sun-yuchen-writing)** —— 启发了 **Narrator Gap**（叙述者相信的 vs 行为事实 vs 读者结论的三列表）、**素材账本**（数字 / 物件 / 劳动账本化）、**审稿工作流**（百分制量表 + 删留补换）与 **Skill 工程结构**（渐进加载、agents 配置）。

本项目不是两者的合并或改写，而是在此基础上重新组织的第三个模型：

```text
Reader State（控制层）
    ↓
Unbuyable Gap（本项目核心差异：财富失效的位置）
    ↓
Evidence（六类账本：Numbers / Objects / Labor / Space / Transactions / Actions）
```

与两项目的区别要点：

- **Unbuyable Gap 取代"双层故事"作为故事命题层**：目标不是"表层钱 + 深层情感"，而是"资源能解决的事 vs 只有本人能做的事"的对峙。
- **Evidence 扩展为六类**：在数字 / 物件 / 劳动之外加入 **Space**（缺席的物理化）、**Transactions**（关系停止后系统继续执行）、**Actions**（动作对替代心理解释）。
- **八场景叙事引擎**：Pattern → System → Unbuyable Request → Pattern Break → Aftermath 的骨架，让"系统残余"成为正式场景而不是收尾技巧。
- **写作流程严格内部化**：Write Mode 只在 Agent 内部跑完整模型，输出只有标题 + 正文。

本项目未复制来源仓库的独特句子、连续示例情节或完整原文。示例与文案均为原创。

## Philosophy

钱可以解决几乎所有流程，但解决不了在场。**在场**无法外包：不能由助理出席，不能由律师代答，不能由司机抵达。

这个 Skill 不相信"克制"是一种语气。它相信克制是一种**分配**——把情绪分配到证据里，把缺席分配到空间里，把结论分配到读者手里。

> 财富解决表层事件。<br>
> 故事发生在财富失效的位置。

## License

[MIT](LICENSE)。
