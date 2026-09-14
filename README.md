<div align="center">

# 我是产品经理，喜欢做点 AI native 的事

**AI Agent 产品经理** · 能自己动手写点插件

</div>

---

工作之外，我喜欢自己动手做点小东西 —— 不为别的，就是想知道这东西到底长什么样。

**给 agent 做插件，是我目前找到的最好的了解方式。**

插件得像积木一样接得上 agent。想接得上，就得先知道 agent 现在是什么形状：工具调用怎么触发、
权限在哪一层拦、上下文怎么进怎么出、出错的时候人会卡在哪一步。这些读文档看不出来，
得自己插一块上去试。

下面几块就是我插过的。

## 做过的项目

| 项目 | 是什么 |
| :--- | :--- |
| **[voiceshell-os](https://github.com/goldgish/voiceshell-os)** | 不看屏幕的语音外壳：说一句话，agent 把活干完，再用语音讲给你听 |
| **[dsh-gamepad-approval](https://github.com/goldgish/dsh-gamepad-approval)** | 拿 Xbox 手柄审批 agent 的高危操作，A 批准 / B 驳回 · 已发布 npm |
| **[dsh-agent-trace](https://github.com/goldgish/dsh-agent-trace)** | 把 agent 的推理过程和工具调用画成一张图，看懂它在干什么 |
| **[kouyu-ceping](https://github.com/goldgish/kouyu-ceping)** | 口语测评：上传一段音视频，逐字打分并给出改进建议 |

前三个是我自己写着玩的，都是 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 的插件。
kouyu-ceping 不一样 —— 那个是帮别人解决实际问题做的。

voiceshell-os 里顺手做了一套评测：A 层 9 项硬指标 + B 层 5 维评审，跑器和用例集都在仓库里，
clone 下来能直接复跑。语音场景下用户不看屏幕，「什么时候该说话」本身就是产品，不测就没法调。

---

<div align="center">

[![npm](https://img.shields.io/npm/v/dsh-gamepad-approval?style=flat-square&label=npm&color=CB3837)](https://www.npmjs.com/package/dsh-gamepad-approval)
[![last commit](https://img.shields.io/github/last-commit/goldgish/voiceshell-os?style=flat-square&label=%E6%9C%80%E8%BF%91%E6%9B%B4%E6%96%B0&color=4D6BFE)](https://github.com/goldgish/voiceshell-os)
[![license](https://img.shields.io/github/license/goldgish/voiceshell-os?style=flat-square&label=%E8%AE%B8%E5%8F%AF&color=3FB950)](https://github.com/goldgish/voiceshell-os/blob/main/LICENSE)

📮 邮箱待填 · 💻 [github.com/goldgish](https://github.com/goldgish)

</div>
