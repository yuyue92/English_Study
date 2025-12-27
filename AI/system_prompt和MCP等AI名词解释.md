一句话解释：
- system prompt 和 user prompt 是“说话规则与需求”；
- AI agent 是“能够自主干活的AI助手”；
- Agent tools、function calling 是“AI的手和工具”；
- MCP 是“统一、可扩展的工具接入协议”；

它们的大致关系如下：
```
人
 └── User Prompt（你说你要干嘛）
      ↓
AI（LLM）
 ├── System Prompt（它被要求成为什么、怎么做）
 └── AI Agent（有目标、会规划）
       ├── 思考 / 计划
       ├── Function Calling
       ├── Agent Tools
       └── MCP（更高级、标准化的工具体系）
```

一、system prompt（系统提示词），是给AI设定“身份、行为规则、边界”的指令；他不是用户看到的聊天内容，而是系统层的隐形说明书；

二、user Prompt（用户提示词）：就是你对AI说的话；

三、AI Agent = LLM + 目标+ 记忆+ 规划+ 行动能力；它不只是“回答问题”，而是：
- 有目标
- 会分解任务
- 会调用工具
- 会根据结果继续下一步

2️⃣ 通俗比喻（非常关键）

- | 普通 LLM    | AI Agent  |
| --------- | --------- |
| 像“百科全书”   | 像“助理/实习生” |
| 你问一句，它答一句 | 你给目标，它自己干 |
| 不会主动行动    | 会规划、执行、检查 |

一个Agent的典型流程如下：
```
目标：帮用户生成一份 API 设计文档
1. 理解目标
2. 拆解步骤
   - 确定接口
   - 设计字段
   - 写示例
3. 调用工具（如代码生成、数据库）
4. 整合结果
5. 输出
```

四、Agent tools（Agent工具）：是AI可以“真正调用”的外部能力；比如：查数据库、发送http请求、读文件、跑代码、搜索网页’

通俗比喻：AI Agent = AI的手和脚；

五、function calling（函数调用）：是LLM调用工具的一种机制；重点一句话：AI不直接执行函数，而是“决定要不要调用 + 用什么参数”；

六、MCP（Model Context Protocol），MCP= 一套让AI标准化接入“外部能力”的协议；一句话：function calling的“升级版 + 工业标准版”；

七、把所有概念串成一句话
- System Prompt 定义 AI 是谁，
- User Prompt 告诉 AI 要做什么，
- AI Agent 决定怎么做，
- Function Calling 让 AI 能调用函数，
- Agent Tools 是函数集合，
- MCP 是统一、可扩展的工具协议。
