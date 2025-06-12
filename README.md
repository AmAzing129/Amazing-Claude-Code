# Claude-Code-Best-Practices

## 版本 1.0.21

https://www.anthropic.com/claude-code

- 集成到 IDE 中 https://docs.anthropic.com/en/docs/claude-code/ide-integrations

### [对话历史管理](https://docs.anthropic.com/en/docs/claude-code/tutorials#resume-previous-conversations)

如果重启了终端:

- `claude --continue` 直接恢复最近一次对话
- `claude --resume` 可以查看对话历史 

### [使用图片](https://docs.anthropic.com/en/docs/claude-code/tutorials#work-with-images)

- [ ] 目前使用 Snipaster 直接粘贴不了
- 本地文件可以直接拖拽进去

### 长对话流程管理

- `/compact [instructions]` 根据指令阶段性总结
- 双击 ESC 可以跳转到某一条消息，并且 fork 一个新对话出来

### MCP

- [Figma](https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Dev-Mode-MCP-Server)
  `claude mcp add --transport sse figma-dev-mode-mcp-server http://127.0.0.1:3845/sse`

### [创建自定义命令](https://docs.anthropic.com/en/docs/claude-code/tutorials#create-custom-slash-commands)

- 相当于团队共享提示词
