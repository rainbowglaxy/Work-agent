# 多模型群聊编排台 · AgentGroupChat

一个 Windows 桌面客户端：把**不同厂商的大模型**拉进同一个"群聊"，按角色分工协作，共同完成你的任务。

> 相当于给多个模型建了一个群：调度官决定谁发言，各模型按 需求 → 设计 → 评审 → 编码 → 汇总 的流程接力产出。

## 成员与接入方式

| 成员 | 厂商 | 接入通道 | 角色 |
|---|---|---|---|
| GPT-5 | OpenAI | API | 需求分析师 |
| Claude | Anthropic | API | 方案架构师 |
| Gemini | Google | API | 技术评审 |
| 智谱 GLM | 智谱AI | API | 资料 / 数据 |
| Codex | OpenAI CLI | CLI 无头命令（`codex exec`） | 工程师 · 落地 |
| 调度官 | — | GroupChatManager | 决定下一位发言者 |

没有 API 的模型（如 Codex）通过 **CLI 适配器**接入：轮到它时由编排器执行 `codex exec "任务"` 并回收结果。

## 技术栈

- 壳：Electron
- 渲染：原生 HTML / CSS / JS（单文件，无构建）
- 编排引擎（待接入）：Python · AutoGen GroupChat
- 协议：A2A（跨服务器智能体协作时）

## 开发与运行

```bash
npm install
npm start
```

## 打包成 Windows 成品

```bash
npm run build
# 产物在 dist/AgentGroupChat-Portable.exe（免安装，双击运行）
```

## 当前状态

- [x] 桌面端壳 + 三栏控制台 UI（成员 / 群聊 / 协作流程）
- [x] 群聊编排流程演示与产出代码
- [x] 接入真实模型配置面板
- [ ] 接入真实 LLM API（多厂商混搭）
- [ ] 接入 Codex CLI 适配器
- [ ] 任务持久化与历史记录

## License

MIT

## Maintainer and security

Created and maintained by **Weixing Liu (刘卫星)**, GitHub **[rainbowglaxy](https://github.com/rainbowglaxy)**. I maintain the project and handle security reports, dependency maintenance, and security fixes.

See [SECURITY.md](SECURITY.md) for the security reporting policy and the scope of defensive security review.
