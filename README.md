<div align="center">

# 给 agent 造接口，也造验收

**AI Agent 产品经理** · 产品出身，能自己写插件

做的都是同一件事：让 agent 从「demo 很惊艳」走到「日常敢用」

</div>

---

agent 的能力早就不是瓶颈了，卡住的是**人机接口**。

- 它做完事了，但你得**回到屏幕前**才知道做没做完
- 它要动危险操作，审批却逼你切窗口、点鼠标
- 它想了四十秒，你看不出它在干活还是在死循环
- 而这条通道本身靠不靠谱，得有办法量出来

这几个题，我各做了一遍。

## 精选项目

| 项目 | 通道 | 解决什么 |
| :--- | :--- | :--- |
| **[voiceshell-os](https://github.com/goldgish/voiceshell-os)** · 声壳 | 输出 | 说一句话，全程不看屏幕。10 例真实任务实测：首声 1.3–3.0s、回合完成度 10/10、B 层评审均分 4.78/5 |
| **[dsh-gamepad-approval](https://github.com/goldgish/dsh-gamepad-approval)** | 审批 | 高危操作要过手柄物理按键，A 批 / B 驳。18 条规则，无手柄即驳回（fail-closed）· 已发布 npm |
| **[dsh-agent-trace](https://github.com/goldgish/dsh-agent-trace)** | 观察 | 把 agent 的推理链与并行工具调用，画成可交互的 DAG |
| **[kouyu-ceping](https://github.com/goldgish/kouyu-ceping)** | 验收 | 口语测评：上传音视频 → 逐字打分 → LLM 生成改进建议 |

前三个是 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 插件，挂在同一个 TUI 上，各占一个通道，互不干扰。

## 我怎么做事

**① 先定「什么算好」，再动手改。**
voiceshell-os 的评测标准是公开的 —— A 层 9 项硬指标（门槛制，任一不过即整例失败）+ B 层 5 维评审（1–5 分）。跑器、用例集、防回归自测一并入库，clone 下来就能复跑。数字不是我说的，是跑出来的。

**② 假绿比红更危险。**
这个项目迭代五轮，其中三次「全绿」其实是误判：TTS 顶断把 38 字的答案掐在 1.1 秒；判词表太窄，把「域名解析不了」这种正确行为判成了失败；线上提示词比测试侧少了整批规则，导致长任务静默 50 秒。三件事都写进仓库的复盘章节了。

**③ 播报即产品。**
语音场景里用户不看屏幕，说话就是唯一反馈通道。所以「什么时候该开口」是产品设计，不是日志打印 —— 播报有配额、有禁区、35 秒没动静必须出声、不可逆操作先问再动。

---

<div align="center">

[![npm](https://img.shields.io/npm/v/dsh-gamepad-approval?style=flat-square&label=npm&color=CB3837)](https://www.npmjs.com/package/dsh-gamepad-approval)
[![last commit](https://img.shields.io/github/last-commit/goldgish/voiceshell-os?style=flat-square&label=%E6%9C%80%E8%BF%91%E6%9B%B4%E6%96%B0&color=4D6BFE)](https://github.com/goldgish/voiceshell-os)
[![license](https://img.shields.io/github/license/goldgish/voiceshell-os?style=flat-square&label=%E8%AE%B8%E5%8F%AF&color=3FB950)](https://github.com/goldgish/voiceshell-os/blob/main/LICENSE)

**想聊 agent 的产品化、或者接口层怎么做，随时找我。**

📮 邮箱待填 · 💻 [github.com/goldgish](https://github.com/goldgish)

</div>
