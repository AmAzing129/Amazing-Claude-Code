# Claude-Code-Best-Practices v1.0.22

https://www.anthropic.com/claude-code

https://github.com/anthropics/claude-code

## 开始使用

- 安装到 ~/.claude/local/claude 获取自动更新
- 集成到 IDE 中 https://docs.anthropic.com/en/docs/claude-code/ide-integrations
- 价格：Token 按量计费或者 [Max](https://support.anthropic.com/en/articles/11014257-about-claude-s-max-plan-usage)
- 建议：不定期使用采用 Token，定期使用 Pro 会更优惠，深度使用 Max 用量足够

## 概念
- **message** 一条发送给 Claude 的消息
- **conversation** 在不清空上下文或重启终端情况下的持续对话
- **session**: A "session" starts with your first message to Claude and lasts for 5 hours.

  从某一时刻向 Claude 发送的第一条消息开始，持续 5 小时。在这 5 小时内再发送任何消息都算作同一个会话。5 小时会重置

## 使用习惯
- Plan your work around the 5-hour reset period 以 5 小时为工作周期。刚好对应上午、下午、晚上 
- [应对限额的最佳实践](https://support.anthropic.com/en/articles/9797557-usage-limit-best-practices)

## 终端
- 退出终端 `/exit` `/quit` 或者两次 `Ctrl + C`

## 对话

- `/clear` 新开一个对话，释放上下文

### [对话历史管理](https://docs.anthropic.com/en/docs/claude-code/tutorials#resume-previous-conversations)

如果重启了终端:

- `claude --continue` 直接恢复最近一次对话
- `claude --resume` 可以查看对话历史 

### [使用图片](https://docs.anthropic.com/en/docs/claude-code/tutorials#work-with-images)

- [ ] 目前使用 Snipaster 直接粘贴不了
- 本地文件可以直接拖拽进去

### 长对话流程管理

- `/compact [instructions]` 根据指令阶段性总结
- 双击 ESC 查看消息历史，可以跳转到某一条消息，并且 fork 一个新对话出来

### MCP

- [Figma](https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Dev-Mode-MCP-Server)
  `claude mcp add --transport sse figma-dev-mode-mcp-server http://127.0.0.1:3845/sse`

### [创建自定义命令](https://docs.anthropic.com/en/docs/claude-code/tutorials#create-custom-slash-commands)

- 把常用消息封装为一个指令，可以个人使用，或者仓库级别团队共享。

### 有需求但暂不支持或未发现的功能

- 希望在命令行内查看对话历史，每次需要退出去执行 `claude --resume`
