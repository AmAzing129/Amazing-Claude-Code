# Amazing-Claude-Code v1.0.41

https://www.anthropic.com/claude-code

https://github.com/anthropics/claude-code

## 开始使用

- 安装到 ~/.claude/local/claude 获取自动更新
- 集成到 [IDE](https://docs.anthropic.com/en/docs/claude-code/ide-integrations) 中，不必抛弃你的 Cursor，然后就会发现，你不需要切换 tab 了
  <img width="799" alt="image" src="https://github.com/user-attachments/assets/ffa95410-3c06-4766-ae2d-b6ff79ee53b3" />
- 价格：Token 按量计费或者 [Max](https://support.anthropic.com/en/articles/11014257-about-claude-s-max-plan-usage)
- 建议：不定期使用采用 Token，定期使用 Pro 会更优惠，深度使用 Max 用量足够 [查看用量](https://github.com/ryoppippi/ccusage)

## 概念
- **message** 一条发送给 Claude 的消息
- **conversation** 在不清空上下文或重启终端情况下的持续对话
- **session**: A "session" starts with your first message to Claude and lasts for 5 hours.

  从某一时刻向 Claude 发送的第一条消息开始，持续 5 小时。在这 5 小时内再发送任何消息都算作同一个会话。5 小时会重置

## 使用习惯
- Plan your work around the 5-hour reset period 以 5 小时为工作周期。刚好对应上午、下午、晚上 
- [应对限额的最佳实践](https://support.anthropic.com/en/articles/9797557-usage-limit-best-practices)

## 终端
- 在 IDE 中打开 claude `Command + ESC`
- 退出终端 `/exit` `/quit` 或者两次 `Ctrl + C`

## Conversation 对话管理

- `/clear` 新开一个对话，释放上下文

### 对话模式

使用 `shift + tab` 切换，有三种模式
- auto-accept edits on 自动接受更改
- plan mode on 开始前会先提供修改计划
- 正常模式，会一步一步询问

### [对话历史](https://docs.anthropic.com/en/docs/claude-code/tutorials#resume-previous-conversations)

如果重启了终端:

- `claude --continue` 直接恢复最近一次对话
- `claude --resume` 可以查看对话历史
  
  对话历史有三栏，Modified, Created, Messages Summary，按照修改时间排序。如果选择某个历史对话再发消息，该对话将会更新修改时间，创建时间不变。

### 长对话流程管理

- `/compact [instructions]` 根据指令阶段性总结
- 双击 ESC 查看消息历史，可以跳转到某一条消息，并且 fork 一个新对话出来

## Context 上下文管理

### [Memory 记忆](https://docs.anthropic.com/en/docs/claude-code/memory)

- 在使用过程中，不断优化 CLAUDE.md 文件
- 在子文件夹中，比如一个 features 下，也可以放对应的 CLAUDE.md

  Claude will also discover CLAUDE.md nested in subtrees under your current working directory. Instead of loading them at launch, they are only included when Claude reads files in those subtrees.

### 使用文件

- [图片](https://docs.anthropic.com/en/docs/claude-code/tutorials#work-with-images)复制后，使用 `Ctrl + V`（不是 cmd + v）
- 文件可以直接拖拽进去（也包括目录、图片）

### MCP

- [Figma](https://help.figma.com/hc/en-us/articles/32132100833559-Guide-to-the-Dev-Mode-MCP-Server)
  `claude mcp add --transport sse figma-dev-mode-mcp-server http://127.0.0.1:3845/sse`

- [zen](https://github.com/BeehiveInnovations/zen-mcp-server)

## Prompt 提示词管理

### [创建自定义命令](https://docs.anthropic.com/en/docs/claude-code/tutorials#create-custom-slash-commands)

- 把常用消息封装为一个指令，可以个人使用，或者仓库级别团队共享。

## Claude Code 生态

### 用量监控

- [ccusage](https://github.com/ryoppippi/ccusage)
- [Claude-Code-Usage-Monitor](https://github.com/Maciek-roboblog/Claude-Code-Usage-Monitor)
- [ccseva](https://github.com/Iamshankhadeep/ccseva)

### 同时使用其他模型

- [claude-code-router](https://github.com/musistudio/claude-code-router)
- [zen](https://github.com/BeehiveInnovations/zen-mcp-server)

## Reference

[A conversation on Claude Code](https://www.youtube.com/watch?v=Yf_1w00qIKc)
