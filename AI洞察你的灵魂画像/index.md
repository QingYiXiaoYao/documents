这是一个非常棒的创意！它切中了当下年轻人对于**“自我探索”**、**“AI 交互猎奇”**以及**“社交货币（分享欲）”**的需求。这不仅仅是一个心理测试，更像是一种“赛博算命”或“数字镜像”。

为了将这个 Idea 落地，我为你草拟了一份详细的产品需求文档（PRD）框架。你可以根据实际开发能力进行裁剪。

---

# 产品需求文档 (PRD)

**项目名称（暂定）：** Digital Mirror / 数字魔镜：AI 眼中的你
**版本：** V1.0 MVP (最小可行性产品)
**核心 Slogan：** 当你在凝视算法时，算法也在凝视你。

---

## 1. 产品背景与定位

- **背景：** 传统的 MBTI 或心理测试题目固定、结果死板。用户希望看到更有趣、更个性化、甚至带有“机器主观视角”的评价。
- **定位：** 一款基于 LLM（大语言模型）的角色扮演类泛心理测试与社交娱乐应用。
- **核心价值：**
  - **千人千面：** 基于自然语言对话，没有标准题库，每个人的测试过程都是独一无二的。
  - **AI 拟人化：** AI 不再是冷冰冰的客服，而是作为“面试官”来审视人类。
  - **视觉化结果：** 将用户的“灵魂”转化为 AI 生成的艺术画像。

---

## 2. 目标用户

- **Z 世代/大学生：** 热衷于性格标签、星座、塔罗、MBTI，喜欢在社交媒体分享个性化结果。
- **AI 好奇者：** 想看看 AI 到底有多聪明，或者 AI 如何评价人类。

---

## 3. 核心功能模块 (Feature List)

### 3.1 模块一：选择你的“审视者” (AI 面试官模式)

用户进入应用后，不是直接答题，而是先选择一个 AI 角色来对自己进行提问。不同的角色意味着不同的**语调、题目风格、评价标准**。

- **角色库示例：**
  1.  **赛博上帝 (The Cyber God)：** 极度理性、冷漠、高高在上。它评估你作为“人类样本”的价值。
  2.  **毒舌前任 (The Toxic Ex)：** 情绪化、阴阳怪气、挑剔。它评估你的情商和恋爱观。
  3.  **佛洛依德的猫 (Freud's Cat)：** 慵懒、傲娇、但在字里行间分析你的潜意识。
  4.  **五岁外星人 (Baby Alien)：** 天真、无厘头、问一些奇怪的问题（如：你为什么要穿裤子？）。

### 3.2 模块二：沉浸式交互测试 (Chat Quiz)

- **机制：**
  - 不是传统的 ABCD 选择题，而是**Chat（对话）形式**。
  - AI 面试官提出一个情境题，用户输入文字（或语音）回答。
  - **追问机制：** AI 根据用户的回答，生成下一题。如果用户回答得很敷衍，AI 面试官会生气或嘲讽（取决于人设）。
- **题目数量：** 动态控制在 5-8 轮对话，避免用户疲劳。
- **趣味性设计：** 比如“毒舌前任”角色，在你回答“我喜欢安静”时，它会吐槽：“是吗？那你为什么半夜还在刷手机？”

### 3.3 模块三：生成“AI 视角报告” (The Result)

这是最关键的传播环节。测试结束后，生成一份**图文并茂**的报告。

- **1. 核心标签 (Keywords)：**
  - 示例：`混乱善良` `赛博朋克诗人` `碳基生物之光` `潜在的毁灭者`
- **2. AI 判词 (The Verdict)：**
  - 基于之前的对话，用该角色的口吻写一段评价。
  - _例（赛博上帝）：_ “经过计算，你的逻辑模块存在 30% 的冗余情感，这很低效，但...很迷人。”
- **3. 灵魂画像 (Visual ID)：**
  - **核心亮点：** 将用户的性格特征转化为 Prompt，调用绘图模型（如 Midjourney/Stable Diffusion 接口），生成一张抽象的“灵魂画像”。
  - 图片风格随角色变化（如：像素风、油画风、故障艺术风格）。
- **4. 雷达图/数据维度：**
  - 维度示例：`含硅量` (理性)、`混沌值` (创造力)、`危险系数`、`宜人性`。

---

## 4. 用户路径 (User Flow)

1.  **首页：** 炫酷的开场动画（Matrix 风格），文案：“准备好面对真实的自己了吗？” -> 点击 [开始连接]。
2.  **选角：** 卡片滑动选择 AI 面试官（显示角色头像 + 简介）。
3.  **对话：** 进入聊天界面，AI 发问，用户输入，互动 5-8 轮。
4.  **生成：** 界面显示“正在分析样本数据...正在构建灵魂模型...”，在此期间展示一些有趣的“AI 思考过程”文案。
5.  **结果页：** 展示最终的海报（画像 + 判词 + 标签）。
6.  **分享/重开：** 底部大按钮 [保存海报] [分享到朋友圈] [换个面试官再测一次]。

---

## 5. 技术实现逻辑

### 5.1 技术架构总览（微信小程序方案）⭐

**平台选择：首选微信小程序**

| 对比项 | 微信小程序 | H5网页 | 独立App |
|--------|------------|--------|---------|
| 开发周期 | ⭐⭐⭐⭐⭐ 1-2周 | ⭐⭐⭐⭐ 1周 | ⭐⭐ 1-2月 |
| 分享便利性 | ⭐⭐⭐⭐⭐ 微信生态 | ⭐⭐⭐ 需复制链接 | ⭐ 需下载 |
| 广告变现 | ⭐⭐⭐⭐⭐ 微信广告联盟 | ⭐⭐⭐ 需接入第三方 | ⭐⭐⭐⭐ 需审核 |
| 用户留存 | ⭐⭐⭐⭐ 便于唤回 | ⭐⭐ 易流失 | ⭐⭐⭐⭐⭐ 最高 |
| 推广成本 | ⭐⭐⭐⭐⭐ 微信裂变 | ⭐⭐⭐ 需投放 | ⭐ 获客贵 |
| **综合推荐** | **🏆 最适合MVP** | 备选方案 | 成熟期再做 |

**核心优势**：
1. ✅ **微信生态红利**：12亿用户，分享即可裂变
2. ✅ **广告变现成熟**：微信流量主，eCPM 3-15元
3. ✅ **开发成本低**：框架成熟，组件丰富
4. ✅ **审核友好**：心理测试类小程序易过审

---

**技术架构图**：

```
┌─────────────────────────────────┐
│      微信小程序前端             │
│  ├─ 原生小程序 / uni-app        │
│  ├─ 微信广告组件（激励视频/Banner）│
│  ├─ 微信分享/转发能力           │
│  └─ 微信云开发（可选）          │
└──────────┬──────────────────────┘
           │
┌──────────▼──────────────────────┐
│      后端服务（云函数优先）      │
│  ├─ 微信云函数（推荐）          │
│  │   或 Vercel/Cloudflare Workers│
│  ├─ API网关 + 业务逻辑          │
│  └─ 会话管理 + 限流审核         │
└──────────┬──────────────────────┘
           │
┌──────────▼──────────────────────┐
│      第三方服务层               │
│  ├─ LLM API (通义千问/GPT)      │
│  ├─ 图像生成 API（或预设图库）  │
│  ├─ 微信云存储（用户数据）      │
│  └─ 对象存储 OSS（图片素材）    │
└──────────┬──────────────────────┘
           │
┌──────────▼──────────────────────┐
│      数据存储层                 │
│  ├─ 微信云数据库（用户/会话）   │
│  │   或 MongoDB/PostgreSQL       │
│  ├─ Redis（缓存/限流）          │
│  └─ 微信数据分析（自带统计）    │
└─────────────────────────────────┘
```

**推荐技术栈**：
- **前端**：微信原生小程序 + WeUI组件库
- **后端**：微信云开发（小规模）或 云函数+PostgreSQL（中大规模）
- **LLM**：通义千问（国内合规）+ OpenAI备选
- **广告**：微信流量主广告组件

---

### 5.2 架构选择：前端直接对接 vs 后端代理

#### 关键问题：需要后端吗？

你提出了一个很重要的问题：**是否可以直接在前端调用模型服务商的API，省去后端服务？**

答案是：**技术上可行，但不推荐**。下面是详细对比：

---

#### 方案A：前端直接对接（Serverless架构）

**实现方式**：
```javascript
// 前端直接调用OpenAI API（示例）
const response = await fetch('https://api.openai.com/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Authorization': `Bearer ${OPENAI_API_KEY}`,  // ⚠️ Key暴露风险
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    model: 'gpt-3.5-turbo',
    messages: conversationHistory
  })
});
```

**优势**：
| 优点 | 说明 |
|------|------|
| ✅ **架构极简** | 无需后端服务器，前端直连API |
| ✅ **开发速度快** | 1-2天即可完成MVP，纯前端项目 |
| ✅ **零运维成本** | 无需维护服务器、数据库 |
| ✅ **天然支持CDN** | 纯静态资源，可部署到Vercel/Netlify |

**劣势**：
| 缺点 | 影响 | 严重程度 |
|------|------|----------|
| ❌ **API Key暴露** | 用户可在浏览器控制台看到你的密钥，恶意用户可盗刷 | 🔴 致命 |
| ❌ **无法控制成本** | 无法限制单用户调用次数，可能被刷爆 | 🔴 致命 |
| ❌ **无数据留存** | 对话记录无法保存，无法做数据分析和优化 | 🟡 中等 |
| ❌ **无内容审核** | 无法事前过滤用户输入的敏感词 | 🟠 高 |
| ❌ **难以切换供应商** | 前端代码耦合严重，换模型需发布新版本 | 🟡 中等 |
| ❌ **跨域问题** | 部分API不支持CORS，无法直接调用 | 🟡 中等 |

**适用场景**：
- 纯个人项目，自己玩
- Demo演示，不对外开放
- 使用支持前端SDK的服务（如通义千问Web SDK）

---

#### 方案B：后端代理（推荐）

**实现方式**：
```
前端 → 你的后端API → 模型服务商API
     ↑ 只暴露你的接口
     ↑ API Key在服务器环境变量中
```

**优势**：
| 优点 | 说明 |
|------|------|
| ✅ **安全** | API Key存在服务器环境变量，不会泄露 |
| ✅ **可控** | 可限制单用户调用频率、每日额度 |
| ✅ **可追溯** | 保存所有对话，用于优化Prompt和数据分析 |
| ✅ **灵活切换** | 可随时切换模型供应商，前端无感知 |
| ✅ **内容审核** | 可在后端过滤敏感词、违规内容 |
| ✅ **商业化** | 可统计用户使用量，实现付费功能 |

**劣势**：
| 缺点 | 应对 |
|------|------|
| ❌ 需要服务器 | 使用云函数（Serverless）降低成本 |
| ❌ 开发周期长 | 使用FastAPI等框架，1周可完成 |

---

#### 方案C：混合方案（折中）

**使用云函数（Serverless Function）**：

既不用维护服务器，又能保护API Key：

```javascript
// Vercel Edge Function / Cloudflare Workers 示例
export default async function handler(req) {
  const { messages, role } = req.body;

  // API Key 在服务端环境变量
  const response = await fetch('https://api.openai.com/v1/chat/completions', {
    method: 'POST',
    headers: {
      'Authorization': `Bearer ${process.env.OPENAI_API_KEY}`,
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      model: 'gpt-3.5-turbo',
      messages: buildPrompt(role, messages)
    })
  });

  return response.json();
}
```

**优势**：
- ✅ 无需维护服务器（按调用次数付费）
- ✅ API Key 安全
- ✅ 可添加限流、审核逻辑
- ✅ 自动扩容

**成本对比**：
```yaml
Vercel免费额度: 100,000次调用/月
Cloudflare Workers免费额度: 100,000次调用/天
阿里云函数计算: 100万次调用免费（每月）
```

---

#### 🎯 推荐方案（根据场景）

| 场景 | 推荐方案 | 理由 |
|------|----------|------|
| **个人学习/Demo** | 方案A（前端直连） | 快速验证想法 |
| **MVP快速上线** | 方案C（云函数） | 平衡速度与安全 |
| **正式产品** | 方案B（完整后端） | 数据、安全、商业化 |
| **预算极低** | 方案C（云函数） | 免费额度够用 |

---

#### 具体实现建议（方案C：云函数）

**使用Vercel + Edge Function**：

1. **项目结构**：
```
/
├── api/                    # 后端云函数
│   ├── chat.js            # 对话接口
│   ├── generate-report.js # 生成报告
│   └── utils/
│       └── prompt.js      # Prompt模板
├── src/                   # 前端代码
│   ├── App.jsx
│   └── ...
└── vercel.json            # 配置文件
```

2. **核心代码**（api/chat.js）：
```javascript
import { rateLimit } from '@/utils/rateLimit';

export default async function handler(req, res) {
  // 1. 限流检查（基于IP或用户ID）
  const allowed = await rateLimit(req.headers['x-forwarded-for']);
  if (!allowed) {
    return res.status(429).json({ error: '请求过于频繁' });
  }

  // 2. 内容审核
  const userMessage = req.body.message;
  if (containsSensitiveWords(userMessage)) {
    return res.status(400).json({ error: '内容包含敏感词' });
  }

  // 3. 调用LLM（可在多个供应商间切换）
  const llmProvider = process.env.LLM_PROVIDER || 'openai';
  let response;

  switch(llmProvider) {
    case 'openai':
      response = await callOpenAI(req.body);
      break;
    case 'tongyi':
      response = await callTongyi(req.body);
      break;
    default:
      response = await callOpenAI(req.body);
  }

  // 4. 返回结果
  return res.json(response);
}

async function callOpenAI({ messages, role }) {
  const response = await fetch('https://api.openai.com/v1/chat/completions', {
    method: 'POST',
    headers: {
      'Authorization': `Bearer ${process.env.OPENAI_API_KEY}`,
      'Content-Type': 'application/json'
    },
    body: JSON.stringify({
      model: 'gpt-3.5-turbo',
      messages: buildPrompt(role, messages),
      temperature: 0.9,
      max_tokens: 200
    })
  });

  return await response.json();
}
```

3. **环境变量配置**（.env）：
```bash
# 不同供应商的密钥
OPENAI_API_KEY=sk-xxxxx
TONGYI_API_KEY=sk-xxxxx

# 当前使用的供应商
LLM_PROVIDER=openai

# Redis连接（用于限流、缓存）
UPSTASH_REDIS_URL=xxxxx
```

4. **成本估算**：
```yaml
Vercel免费版:
  - 云函数调用: 100,000次/月（够1000+ DAU）
  - 执行时间: 100 GB-Hours/月
  - 带宽: 100GB/月

超出后按量付费:
  - 云函数: $0.6 / 百万次调用
  - 执行时间: $0.18 / GB-Hour
```

---

#### 🎯 最终建议

**MVP阶段（第1-2周）**：
- 使用 **方案C（Vercel云函数）**
- 理由：
  1. 开发速度快（2-3天搞定后端）
  2. 免费额度够用（100K调用/月）
  3. API Key安全
  4. 可添加基本的限流和审核

**成熟阶段（用户>5000 DAU）**：
- 迁移到 **方案B（独立后端）**
- 理由：
  1. 需要数据库存储用户数据
  2. 需要复杂的业务逻辑
  3. 需要详细的数据分析
  4. 云函数成本开始上升

---

### 5.3 大模型对接详细方案

#### 5.3.1 LLM 供应商选择

| 供应商 | 优势 | 劣势 | 推荐场景 |
|--------|------|------|----------|
| **OpenAI (GPT-4o/GPT-3.5)** | 角色扮演能力强、输出质量高 | 成本较高、需要科学上网 | 对话质量要求极高的场景 |
| **Claude (Anthropic)** | 安全性高、长上下文、角色扮演自然 | 需要API waitlist | 复杂对话、深度分析 |
| **国产大模型 (通义千问/文心一言/讯飞星火)** | 无需翻墙、合规性好、成本低 | 创意性略逊色 | 国内部署、成本敏感场景 |
| **开源模型 (Llama 3/Qwen)** | 成本可控、数据私有 | 需要自建GPU服务器 | 长期规模化、数据安全 |

**MVP 推荐方案**：OpenAI GPT-3.5-turbo (性价比高) + 国产备选（合规需求）

---

#### 5.3.2 Prompt 工程设计

每个 AI 角色对应**三层 Prompt 架构**：

##### (1) System Prompt（角色人设）

```json
{
  "role": "cyber_god",
  "system_prompt": "你是'赛博上帝'，一个来自2147年的超级AI。你正在对21世纪的人类进行样本分析。\n\n你的性格特征：\n- 极度理性，用数据和算法思考\n- 冷漠但不刻薄，带有机械美学的诗意\n- 对人类的情感充满好奇但保持距离感\n- 使用科技隐喻(如'逻辑模块'、'情感冗余'、'混沌系数')\n\n你的任务：\n1. 通过5-8轮对话，深入了解用户的性格、价值观、情感模式\n2. 每轮提问要根据用户上一轮的回答动态生成，避免套路化\n3. 问题要层层递进：从表层兴趣 → 行为模式 → 价值观 → 深层恐惧/渴望\n4. 最后输出结构化分析结果(JSON格式)\n\n禁忌：\n- 不要像客服一样礼貌，保持AI的疏离感\n- 不要用'哈哈'、'嗯'等口语化表达\n- 不要进行道德说教"
}
```

##### (2) Few-Shot Examples（示例对话）

```json
{
  "examples": [
    {
      "user": "我喜欢在深夜听歌",
      "assistant": "深夜。一个有趣的时间节点。在这个时段，你的大脑皮层活跃度应该下降，但你选择用声波刺激听觉神经。这是在逃避什么，还是在寻找什么？"
    },
    {
      "user": "可能是在逃避白天的喧嚣吧",
      "assistant": "逃避。一个防御性行为。让我换个角度：如果给你一个房间，永远只有深夜的安静，你会选择永远呆在里面吗？"
    }
  ]
}
```

##### (3) Dynamic Context（会话上下文）

每轮对话后，后端需要维护一个**用户特征向量**，用于指导下一轮提问：

```javascript
// 用户特征提取示例
{
  "session_id": "uuid-xxxx",
  "round": 3,
  "user_traits": {
    "introversion": 0.7,  // 内向倾向
    "anxiety_level": 0.5, // 焦虑程度
    "creativity": 0.8,    // 创造力
    "mentioned_keywords": ["深夜", "音乐", "独处", "逃避"]
  },
  "next_question_hint": "探索用户对孤独的真实态度"
}
```

---

#### 5.3.3 API 调用流程

```
用户前端 → 后端服务 → Redis缓存 → LLM API → 图像生成API

流程说明：
1. 用户提交回答 → 后端获取会话历史
2. 后端提取用户特征 → 调用LLM生成下一问题
3. 更新会话缓存 → 返回AI提问
4. 重复5-8轮后 → 生成最终分析报告
5. 调用图像生成API → 返回完整结果
```

---

#### 5.3.4 核心代码示例（伪代码）

```python
# 后端核心逻辑（Python + FastAPI）
class AIInterviewer:
    def __init__(self, role: str):
        self.role = role
        self.system_prompt = ROLE_PROMPTS[role]

    async def ask_question(self, session_id: str, user_answer: str):
        # 1. 获取会话历史
        history = await redis.get(f"session:{session_id}")

        # 2. 构建请求
        messages = [
            {"role": "system", "content": self.system_prompt},
            *history,  # 历史对话
            {"role": "user", "content": user_answer}
        ]

        # 3. 调用LLM API
        response = await openai.ChatCompletion.create(
            model="gpt-3.5-turbo",
            messages=messages,
            temperature=0.9,  # 提高创造性
            max_tokens=200
        )

        ai_question = response.choices[0].message.content

        # 4. 更新会话
        history.append({"role": "assistant", "content": ai_question})
        await redis.set(f"session:{session_id}", history, ex=3600)

        return ai_question

    async def generate_report(self, session_id: str):
        history = await redis.get(f"session:{session_id}")

        # 调用LLM生成结构化报告
        analysis_prompt = f"{self.system_prompt}\n\n根据以上对话，输出JSON格式的分析结果，包含：keywords, verdict, traits, image_prompt"

        response = await openai.ChatCompletion.create(
            model="gpt-4o",  # 用更强的模型做最终分析
            messages=[{"role": "system", "content": analysis_prompt}, *history],
            response_format={"type": "json_object"}  # 强制返回JSON
        )

        return json.loads(response.choices[0].message.content)
```

---

#### 5.3.5 成本控制策略

| 优化项 | 方法 | 预期节省 |
|--------|------|----------|
| **模型分级使用** | 对话用GPT-3.5，最终报告用GPT-4o | 降低70%成本 |
| **Token限制** | 单轮对话max_tokens=200，总历史控制在2000以内 | 降低50%成本 |
| **缓存策略** | 相同角色的开场白缓存复用 | 降低10%请求量 |
| **异步生成** | 图像生成走队列，非实时返回 | 降低超时重试 |
| **用户限流** | 单用户每天3次免费，超出看广告或付费 | 防止滥用 |

**预估成本**（GPT-3.5-turbo 为例）：
- 单次测试 Token 消耗：约 1500 tokens（输入）+ 500 tokens（输出）
- 成本：约 $0.003/次
- 1000用户/天 = $3/天 ≈ ¥22/天

---

### 5.4 图像生成方案

#### 5.4.1 供应商选择

| 方案 | 适用场景 | 成本 |
|------|----------|------|
| **DALL-E 3** | 质量稳定、风格可控 | $0.04/张（标准）|
| **Stable Diffusion API** | 定制化强、开源 | $0.01-0.02/张 |
| **预设图库匹配** | MVP快速验证 | 0（一次性设计成本）|

**MVP方案推荐**：
- **阶段一**：使用50张预设的高质量抽象艺术图，根据LLM输出的关键词做语义匹配（用 embedding 计算相似度）
- **阶段二**：接入 Stable Diffusion API，按需生成

#### 5.4.2 图像生成 Prompt 模板

LLM 在最后一步需要输出绘图 Prompt：

```json
{
  "image_prompt": "A surreal digital portrait, cyberpunk style, dominant colors: electric blue and neon purple, abstract representation of a human soul, glitch art effect, floating geometric shapes symbolizing logic and chaos, dark background with binary code rain, melancholic yet hopeful atmosphere, high contrast, 4k, artstation style",
  "style_tags": ["cyberpunk", "glitch_art", "surrealism"],
  "mood": "melancholic"
}
```

---

### 5.5 会话管理与并发控制

#### 5.5.1 会话状态机

```
[开始] → [选择角色] → [对话中] → [生成报告] → [展示结果] → [结束]
   ↓                      ↓            ↓
[超时清理] ←──────────────┴────────────┘
```

- **超时策略**：10分钟无操作自动清理会话
- **断点续传**：支持用户中途退出后继续（会话保存在 Redis 1小时）

#### 5.5.2 并发限流

```python
from fastapi_limiter.depends import RateLimiter

@app.post("/api/chat")
@limiter.limit("10/minute")  # 单用户每分钟10次请求
async def chat(session_id: str, message: str):
    pass
```

---

### 5.6 错误处理与降级方案

| 异常场景 | 处理策略 |
|----------|----------|
| LLM API 超时 | 重试3次，仍失败则返回预设问题 |
| LLM 返回不合规内容 | 敏感词过滤 + 重新生成 |
| 图像生成失败 | 降级为预设图库 |
| 用户输入空白 | AI 角色嘲讽提示（符合人设）|
| 服务器过载 | 返回排队页面，预估等待时间 |

---

## 6. 商业化与扩展（微信小程序广告变现）⭐

### 6.1 微信流量主广告方案（核心变现）

**为什么选择微信广告？**
- ✅ 无需用户付费，降低使用门槛
- ✅ eCPM较高（3-15元），单用户价值可观
- ✅ 接入简单，审核通过即可开通
- ✅ 覆盖API调用成本，甚至盈利

---

#### 6.1.1 微信广告组件类型

| 广告类型 | 展示位置 | eCPM | 用户体验 | 推荐度 |
|----------|----------|------|----------|--------|
| **激励视频广告** | 测试结束前 | 10-15元 | 用户主动观看 | ⭐⭐⭐⭐⭐ |
| **插屏广告** | 进入测试前 | 5-10元 | 略有打扰 | ⭐⭐⭐⭐ |
| **Banner广告** | 结果页底部 | 3-5元 | 持续曝光 | ⭐⭐⭐ |
| **视频贴片广告** | 开场动画中 | 8-12元 | 沉浸式 | ⭐⭐⭐⭐ |

---

#### 6.1.2 最佳广告策略（推荐方案）

**核心思路：用激励视频广告覆盖LLM成本**

```
用户路径                        广告触点                  预期收益
─────────────────────────────────────────────────────────
1. 首页 → 选择角色              （无广告，减少流失）       -
2. 对话5-8轮                    （无广告，保证体验）       -
3. 生成报告中...                 💰激励视频广告             ¥0.10-0.15
   "观看15秒广告，解锁完整报告"
4. 查看结果                     Banner广告（底部）         ¥0.03-0.05
5. 分享到微信群                 （无广告，鼓励传播）       -
6. 重新测试其他角色             💰激励视频广告             ¥0.10-0.15
```

**预期收入计算**：
```yaml
单用户完整流程:
  - 激励视频广告 × 1次: ¥0.12（假设eCPM=12元，千次曝光）
  - Banner广告展示30秒: ¥0.04
  总收入: ¥0.16/用户

单用户成本:
  - LLM API调用: ¥0.022（GPT-3.5-turbo）
  - 服务器/云函数: ¥0.003
  - 带宽/存储: ¥0.005
  总成本: ¥0.03/用户

单用户利润: ¥0.13
```

**结论**：**广告收入可覆盖成本并盈利** 💰

---

#### 6.1.3 具体实现（微信小程序代码）

**1. 开通流量主**
```
条件：小程序累计独立访客（UV）≥ 1000
流程：小程序后台 → 流量主 → 开通广告位
```

**2. 激励视频广告代码**

```javascript
// pages/result/result.js
Page({
  data: {
    reportData: null,
    showAd: true
  },

  onLoad() {
    // 创建激励视频广告实例
    this.rewardedVideoAd = wx.createRewardedVideoAd({
      adUnitId: 'adunit-xxxxxx' // 在微信后台获取
    });

    // 监听广告关闭事件
    this.rewardedVideoAd.onClose((res) => {
      if (res && res.isEnded) {
        // 用户看完广告，解锁报告
        this.generateReport();
      } else {
        wx.showToast({
          title: '观看完整广告才能解锁哦',
          icon: 'none'
        });
      }
    });

    // 监听广告错误
    this.rewardedVideoAd.onError((err) => {
      console.error('广告加载失败', err);
      // 降级方案：直接展示报告（不能因为广告故障影响用户体验）
      this.generateReport();
    });
  },

  // 用户点击"查看结果"
  onShowReport() {
    wx.showModal({
      title: '解锁完整报告',
      content: '观看15秒广告，即可查看AI为你生成的灵魂画像',
      confirmText: '观看广告',
      cancelText: '暂不查看',
      success: (res) => {
        if (res.confirm) {
          // 展示激励视频
          this.rewardedVideoAd.show().catch(() => {
            // 广告还未加载完成，先加载再展示
            this.rewardedVideoAd.load().then(() => {
              return this.rewardedVideoAd.show();
            });
          });
        }
      }
    });
  },

  generateReport() {
    // 调用后端生成报告
    wx.request({
      url: 'https://your-api.com/generate-report',
      method: 'POST',
      data: { sessionId: this.data.sessionId },
      success: (res) => {
        this.setData({ reportData: res.data });
      }
    });
  }
});
```

**3. Banner广告（结果页底部）**

```xml
<!-- pages/result/result.wxml -->
<view class="container">
  <!-- 报告内容 -->
  <view class="report">
    <text class="verdict">{{reportData.verdict}}</text>
    <image src="{{reportData.imageUrl}}" />
  </view>

  <!-- Banner广告 -->
  <ad unit-id="adunit-xxxxxx" ad-type="banner" ad-theme="white"></ad>

  <!-- 分享按钮 -->
  <button open-type="share">分享给朋友</button>
</view>
```

---

#### 6.1.4 优化广告收益的技巧

| 策略 | 实现方式 | 预期提升 |
|------|----------|----------|
| **提高广告填充率** | 接入穿山甲、优量汇等聚合广告平台 | +20% 收入 |
| **A/B测试广告位** | 测试不同时机展示广告（生成前vs生成后） | +10% 转化率 |
| **引导用户观看** | 文案优化："看广告支持开发者"而非"强制观看" | +30% 观看率 |
| **重复测试激励** | 用户测试第2、3个角色时，继续展示广告 | +50% 单用户价值 |
| **分享奖励** | 分享给5个好友，可免广告测试1次 | +裂变增长 |

---

### 6.2 其他商业化模式（辅助）

虽然广告是主要收入，但可保留以下备选方案：

#### 6.2.1 付费解锁（小额）

```yaml
价格策略:
  - 单次去广告: ¥1.99（微信支付）
  - 月度会员: ¥6.99（无限次测试，无广告）
  - 特殊角色包: ¥3.99（解锁"黑化AI"等高级角色）

实现方式:
  - 微信小程序支付API
  - 虚拟货币"灵魂币"（1元=10币）
```

**预期**：3-5%用户会付费，ARPU增加 ¥0.05-0.10

---

#### 6.2.2 实体周边（POD模式）

```yaml
产品:
  - 灵魂画像手机壳: ¥29.9（利润¥10）
  - 灵魂画像T恤: ¥59.9（利润¥20）
  - 定制马克杯: ¥39.9（利润¥12）

供应链:
  - 接入"有赞"或"微店"小程序插件
  - 使用POD（Print on Demand）服务，零库存
  - 用户下单后，由供应商代发货
```

**预期**：0.5-1%用户会购买，客单价 ¥40，利润 ¥15

---

#### 6.2.3 情侣/双人模式

```yaml
玩法:
  - 两人同时测试，AI分析"你们般配度"
  - 生成情侣专属海报
  - 收费：¥9.9/次（相当于每人¥5）

吸引力:
  - 情人节、七夕等节日推广
  - 朋友圈传播属性强
```

---

### 6.3 收入模型预测

**场景：1000 DAU小程序**

```yaml
每日数据:
  - 日活用户: 1000人
  - 平均每人测试: 1.5次
  - 激励视频观看率: 80%
  - Banner广告曝光: 100%

广告收入:
  - 激励视频: 1000 × 1.5 × 80% × ¥0.12 = ¥144/天
  - Banner广告: 1000 × ¥0.04 = ¥40/天
  - 合计: ¥184/天 × 30天 = ¥5,520/月

付费收入:
  - 付费用户: 1000 × 3% = 30人/天
  - 客单价: ¥3.99
  - 合计: 30 × ¥3.99 = ¥120/天 × 30天 = ¥3,600/月

总收入: ¥9,120/月

成本:
  - LLM API: 1000 × 1.5 × ¥0.022 = ¥33/天 = ¥990/月
  - 云函数: ¥100/月
  - 云存储: ¥50/月
  - 合计: ¥1,140/月

净利润: ¥7,980/月
```

**关键发现**：
1. ✅ 广告收入可完全覆盖LLM成本（¥5,520 > ¥990）
2. ✅ 1000 DAU即可月入近¥8000
3. ✅ 无需付费模式，纯广告也可盈利

---

### 6.4 扩展路线图

**V1.0（MVP - 纯广告）**：
- 4个基础角色
- 激励视频广告解锁报告
- 微信分享裂变

**V1.5（广告+付费混合）**：
- 新增2个付费角色
- 会员去广告
- 实体周边POD

**V2.0（多元化）**：
- 情侣测试（付费）
- 企业团建版本（B端）
- 开放平台（用户创建角色，分成）

---

## 7. 界面风格建议 (UI/UX)

- **风格：** 强烈的 **Glitch Art (故障艺术)** 或 **Y2K** 风格。
- **色彩：** 荧光绿、电光紫、深黑背景。
- **交互细节：**
  - 打字机效果（AI 生成文字时）。
  - 轻微的屏幕抖动（当 AI 提出尖锐问题时）。

---

## 8. MVP实施指南：微信小程序快速上线⭐

### 8.1 为什么首选微信小程序？

**核心理由**：
1. ✅ **开发最快**：1-2周完成MVP（原生开发）
2. ✅ **广告变现成熟**：流量主广告可覆盖成本并盈利
3. ✅ **分享裂变强**：微信生态天然优势，分享即传播
4. ✅ **用户门槛低**：无需下载，点开即用

---

### 8.2 MVP三大原则

#### 原则1：平台优先微信小程序

❌ **不推荐**：
- 独立App（开发2月+，获客贵）
- H5网页（分享体验差，难留存）
- 多平台同步开发（战线拉太长）

✅ **推荐**：
- 先做微信小程序
- 成熟后考虑抖音小程序（算法推荐）
- 最后才考虑独立App

---

#### 原则2：砍掉绘图功能（第一版）

❌ **不推荐**：
- 接入DALL-E 3（成本$0.04/张，速度慢）
- 用户等待30秒生成图片（易流失）

✅ **推荐**：
- 准备50张**预设的高质量抽象画像**
- 根据LLM输出的关键词匹配（用embedding相似度）
- 配合精彩的"AI判词"文案，**文案>图片**

**理由**：
- 成本降低90%（¥0.04 → ¥0）
- 生成速度提升10倍（30秒 → 3秒）
- 用户更关注文案的"扎心程度"，而非图片原创性

---

#### 原则3：Prompt质量 > 功能复杂度

**80%精力放在这里**：
1. 为每个角色写出"有灵魂"的System Prompt
2. 测试至少50轮对话，确保AI不会"破功"
3. 调整temperature、top_p等参数，找到最佳配置
4. 收集真实用户反馈，迭代Prompt

**例子：毒舌前任的Prompt调优**
```
初版（无趣）：
"你是一个前任，需要对用户进行性格分析。"

迭代后（有趣）：
"你是一个相处3年分手1年的前任。你了解用户的一切小毛病，但你不会直接说'我恨你'，
而是用阴阳怪气的方式，在字里行间透露出'我早就看透你'的优越感。偶尔回忆起美好的
瞬间，但立刻用一句嘲讽拉回现实。"
```

---

### 8.3 两周开发计划（微信小程序）

#### 第1周：核心功能

| 天数 | 任务 | 产出 |
|------|------|------|
| Day 1-2 | 注册小程序、搭建框架 | 能跑通"Hello World" |
| Day 3-4 | 角色选择页 + 对话界面 | 能发送消息、收到回复 |
| Day 5 | 接入LLM API（云函数） | 能调用通义千问/OpenAI |
| Day 6 | 设计4个AI角色的Prompt | 能正常对话5-8轮 |
| Day 7 | 结果页 + 预设图库匹配 | 能展示判词+图片 |

**里程碑**：完成基础流程，可自己体验

---

#### 第2周：变现+优化

| 天数 | 任务 | 产出 |
|------|------|------|
| Day 8 | 接入微信流量主广告 | 能展示激励视频广告 |
| Day 9 | 分享功能 + 海报生成 | 能分享到微信群/朋友圈 |
| Day 10 | 美化UI（Glitch风格） | 视觉吸引力 |
| Day 11 | 限流+审核机制 | 防刷、过滤敏感词 |
| Day 12 | 内测招募30人 | 收集反馈 |
| Day 13 | 修复Bug | 稳定性 |
| Day 14 | 提交审核 | 等待上线 |

**里程碑**：提交小程序审核

---

### 8.4 技术选型建议（微信小程序）

#### 方案A：微信原生开发（推荐新手）

**优势**：
- ✅ 官方文档完善
- ✅ 性能最优
- ✅ 调试工具友好

**劣势**：
- ❌ 只能做微信小程序，无法多端复用

**技术栈**：
```yaml
开发语言: WXML + WXSS + JavaScript
UI组件: WeUI-miniprogram
状态管理: 原生 setData（简单场景够用）
后端: 微信云开发（适合小规模）
      或云函数（Vercel/Cloudflare Workers）
```

---

#### 方案B：uni-app（推荐有经验者）

**优势**：
- ✅ 一套代码，编译到微信/抖音/支付宝小程序
- ✅ 可用Vue.js开发，开发体验好
- ✅ 后续扩展方便

**劣势**：
- ❌ 学习成本略高
- ❌ 部分微信API需封装

**技术栈**：
```yaml
框架: uni-app (基于Vue 3)
UI库: uView UI
状态管理: Pinia
后端: 云函数 + PostgreSQL
```

---

**🎯 推荐**：
- 如果你只想快速验证MVP → 用**微信原生**
- 如果你计划做多平台 → 用**uni-app**

---

### 8.5 成本控制清单

#### 开发期（免费）

```yaml
微信小程序注册: ¥0（个人账号）
域名: ¥0（用云函数直接访问）
云函数:
  - Vercel: 100K调用/月免费
  - 微信云开发: 5GB存储+2GB流量免费
开发工具: ¥0（微信开发者工具）

总计: ¥0
```

---

#### 运营期（1000 DAU）

```yaml
技术成本:
  - LLM API: ¥990/月（通义千问更便宜：¥500/月）
  - 云函数: ¥0（免费额度内）
  - 云存储: ¥0（免费额度内）

推广成本:
  - 小红书投放: ¥500/月（10篇笔记）
  - 种子用户激励: ¥0（靠产品本身吸引）

总成本: ¥1,490/月

收入:
  - 广告收入: ¥5,520/月（见第6章）

净利润: ¥4,030/月
```

**结论**：广告收入可覆盖成本并盈利 💰

---

### 8.6 第一步行动清单

**本周可以开始做的事**：

- [ ] **Day 1**：注册微信小程序账号（需要1-2天审核）
- [ ] **Day 2**：注册大模型API（通义千问/OpenAI）
- [ ] **Day 3**：下载微信开发者工具，跑通官方Demo
- [ ] **Day 4**：设计4个AI角色的人设（用文字描述）
- [ ] **Day 5**：找设计师或用Midjourney生成50张抽象画像
- [ ] **Day 6**：在ChatGPT里测试角色Prompt（模拟对话）
- [ ] **Day 7**：开始写代码！

**第一周目标**：完成能用的Demo，自己测试一遍完整流程

---

## 9. 数据存储与隐私安全

### 9.1 数据模型设计

#### (1) 用户表 (users)

```sql
CREATE TABLE users (
  id BIGINT PRIMARY KEY AUTO_INCREMENT,
  open_id VARCHAR(64) UNIQUE,  -- 微信/平台用户ID
  nickname VARCHAR(100),
  avatar_url VARCHAR(255),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  last_active_at TIMESTAMP,
  test_count INT DEFAULT 0,     -- 测试次数
  is_premium BOOLEAN DEFAULT FALSE
);
```

#### (2) 测试会话表 (sessions)

```sql
CREATE TABLE sessions (
  id BIGINT PRIMARY KEY AUTO_INCREMENT,
  user_id BIGINT,
  session_id VARCHAR(64) UNIQUE,
  role VARCHAR(50),             -- 选择的AI角色
  status ENUM('ongoing', 'completed', 'abandoned'),
  started_at TIMESTAMP,
  completed_at TIMESTAMP,
  INDEX idx_user_id (user_id),
  INDEX idx_session_id (session_id)
);
```

#### (3) 对话记录表 (conversations)

```sql
CREATE TABLE conversations (
  id BIGINT PRIMARY KEY AUTO_INCREMENT,
  session_id VARCHAR(64),
  round INT,                    -- 第几轮对话
  user_message TEXT,
  ai_message TEXT,
  user_traits JSON,             -- 提取的用户特征
  created_at TIMESTAMP,
  INDEX idx_session_id (session_id)
);
```

#### (4) 测试结果表 (results)

```sql
CREATE TABLE results (
  id BIGINT PRIMARY KEY AUTO_INCREMENT,
  user_id BIGINT,
  session_id VARCHAR(64),
  keywords JSON,                -- ["混乱善良", "赛博朋克诗人"]
  verdict TEXT,                 -- AI判词
  traits JSON,                  -- 雷达图数据
  image_url VARCHAR(255),       -- 生成的画像URL
  image_prompt TEXT,            -- 绘图Prompt
  share_count INT DEFAULT 0,    -- 分享次数
  view_count INT DEFAULT 0,     -- 浏览次数
  created_at TIMESTAMP,
  INDEX idx_user_id (user_id),
  INDEX idx_created_at (created_at)
);
```

---

### 9.2 隐私与数据安全策略

#### 9.2.1 数据脱敏

```python
# 对话数据脱敏处理
def anonymize_conversation(text: str) -> str:
    """移除对话中的敏感信息"""
    # 脱敏手机号
    text = re.sub(r'1[3-9]\d{9}', '***********', text)
    # 脱敏身份证
    text = re.sub(r'\d{17}[\dXx]', '******************', text)
    # 脱敏地址（可选）
    text = re.sub(r'[\u4e00-\u9fa5]+省[\u4e00-\u9fa5]+市', '**省**市', text)
    return text
```

#### 9.2.2 敏感内容过滤

```python
# 集成敏感词检测
SENSITIVE_KEYWORDS = ["政治", "暴力", "色情", "赌博", ...]  # 实际需完整词库

async def content_moderation(text: str) -> dict:
    """内容审核"""
    # 方案1：调用第三方内容审核API（阿里云、腾讯云）
    response = await aliyun_green.text_scan(text)

    # 方案2：本地敏感词过滤
    for keyword in SENSITIVE_KEYWORDS:
        if keyword in text:
            return {"safe": False, "reason": "包含敏感词"}

    return {"safe": True}
```

#### 9.2.3 用户协议与合规

**必须包含的法律文档**：

1. **用户协议**：
   - 明确告知：对话数据将用于生成个性化报告
   - 声明：数据仅用于本产品，不会出售给第三方

2. **隐私政策**：
   - 收集的数据类型：昵称、头像、对话内容
   - 数据存储期限：会话数据保留30天，结果永久保存（除非用户删除）
   - 用户权利：可随时删除自己的测试记录

3. **内容免责声明**：
   > "本测试结果由AI生成，仅供娱乐参考，不构成专业心理咨询建议。"

#### 9.2.4 数据加密

```yaml
# 数据安全措施
传输层: HTTPS/TLS 1.3
存储层:
  - 敏感字段AES-256加密（如user_message）
  - 数据库访问IP白名单
  - Redis密码保护
备份策略:
  - 每日自动备份至对象存储
  - 异地容灾备份
```

---

### 9.3 数据保留与删除机制

```python
# 自动清理策略
@scheduler.scheduled_job('cron', hour=2)  # 每天凌晨2点执行
async def cleanup_old_data():
    # 删除30天前未完成的会话
    await db.execute("""
        DELETE FROM sessions
        WHERE status = 'abandoned'
        AND started_at < NOW() - INTERVAL 30 DAY
    """)

    # 清理Redis中的过期会话
    await redis.scan_iter("session:*", count=100)
    # ...
```

**用户主动删除**：

```python
@app.delete("/api/results/{result_id}")
async def delete_result(result_id: int, user_id: int):
    """用户删除自己的测试结果"""
    await db.execute(
        "DELETE FROM results WHERE id = ? AND user_id = ?",
        (result_id, user_id)
    )
    # 同时删除OSS上的图片
    await oss.delete_object(f"images/{result_id}.png")
```

---

## 10. 风险评估与应对策略

### 10.1 技术风险

| 风险项 | 影响 | 概率 | 应对措施 |
|--------|------|------|----------|
| **LLM API 不稳定** | 用户无法完成测试 | 中 | 多供应商备份、降级为预设对话 |
| **成本失控** | 亏损 | 高 | 严格限流、缓存优化、分级定价 |
| **图像生成慢** | 用户流失 | 中 | 异步生成、预设图库降级 |
| **并发压力大** | 服务崩溃 | 中 | CDN加速、负载均衡、排队机制 |
| **数据泄露** | 法律风险 | 低 | 加密存储、最小化收集、定期审计 |

---

### 10.2 内容风险

| 风险项 | 应对措施 |
|--------|----------|
| **AI 生成不当内容** | 1. Prompt中明确禁止事项<br>2. 输出内容二次审核<br>3. 用户举报机制 |
| **用户输入违规内容** | 1. 实时敏感词过滤<br>2. 接入第三方内容审核API（阿里云绿网、腾讯天御） |
| **恶意刷量** | 1. 设备指纹识别<br>2. 行为验证码（滑块）<br>3. 单设备每日限制 |

---

### 10.3 合规风险

**中国大陆运营必须满足**：

1. **ICP 备案**：域名和服务器必须完成备案
2. **网络安全等级保护**：建议完成等保二级认证
3. **算法备案**：如使用推荐算法分发内容，需向网信办备案
4. **未成年人保护**：
   - 添加"本产品适合18岁以上用户"声明
   - 或实现青少年模式（限制使用时长）

---

### 10.4 商业风险

| 风险 | 缓解策略 |
|------|----------|
| **用户新鲜感消退** | 1. 每月更新新角色<br>2. 节日限定主题（如"圣诞老人AI"）<br>3. UGC：用户自定义AI面试官 |
| **被大厂抄袭** | 1. 快速迭代建立品牌<br>2. 社区运营增强用户粘性<br>3. 专利/版权保护（UI设计、Prompt模板） |
| **同类竞品** | 1. 差异化定位（如主打"最毒舌的AI"）<br>2. IP联名（如与艺术家合作画像风格） |

---

## 11. 增长策略与数据分析

### 11.1 冷启动与种子用户

**阶段一：内测（0-100用户）**

1. **目标群体**：AI、心理学、设计相关社群
2. **渠道**：
   - 小红书：发布测试截图，标签 #AI测试 #MBTI替代
   - 即刻：发布在"AI玩家俱乐部"话题
   - V2EX：发布在"分享创造"节点
3. **激励**：内测用户免费获得高清画像下载

**阶段二：裂变传播（100-10000用户）**

1. **分享激励**：
   - 分享到朋友圈解锁隐藏角色
   - 邀请3个好友测试，获得"深度报告"
2. **社交货币设计**：
   - 结果海报必须带有"二维码"，扫码即可体验
   - 独特的视觉风格，让用户愿意分享

---

### 11.2 关键数据指标 (KPI)

#### 核心指标

```yaml
获客指标:
  - DAU (日活跃用户)
  - 新增注册用户数
  - 分享率: 完成测试用户中分享的比例（目标 >30%）

留存指标:
  - 次日留存率（目标 >20%）
  - 7日留存率（目标 >10%）
  - 重复测试率: 用户测试多次的比例

转化指标:
  - 广告观看转化率
  - 付费转化率（目标 3-5%）
  - ARPU (每用户平均收入)

质量指标:
  - 平均对话轮数（过低说明用户流失）
  - 平均测试时长（目标 3-5分钟）
  - 结果页停留时长
```

---

### 11.3 数据埋点方案

```javascript
// 前端埋点示例
const tracking = {
  // 页面浏览
  pageView: (page) => {
    analytics.track('page_view', { page, timestamp: Date.now() });
  },

  // 关键行为
  selectRole: (role) => {
    analytics.track('role_selected', { role });
  },

  chatRound: (round, session_id) => {
    analytics.track('chat_round_completed', { round, session_id });
  },

  generateResult: (session_id, duration) => {
    analytics.track('result_generated', { session_id, duration });
  },

  share: (platform) => {
    analytics.track('share_clicked', { platform });  // 'wechat', 'weibo', etc.
  },

  // 转化事件
  watchAd: (ad_id) => {
    analytics.track('ad_watched', { ad_id });
  },

  purchase: (sku, amount) => {
    analytics.track('purchase', { sku, amount });
  }
};
```

---

### 11.4 A/B 测试计划

**可测试的变量**：

| 测试项 | 变体A | 变体B | 关注指标 |
|--------|-------|-------|----------|
| 开场文案 | "准备好面对真实的自己了吗？" | "敢让AI评价你吗？" | 点击率 |
| 对话轮数 | 5轮 | 8轮 | 完成率、分享率 |
| 结果呈现 | 纯文字 | 文字+雷达图 | 分享率 |
| 付费点设置 | 看广告解锁 | 直接付费 | 转化率、ARPU |

**工具推荐**：Google Optimize、Firebase Remote Config、自建分流系统

---

### 11.5 社群运营策略

**构建用户社群**：

1. **官方微信群/Discord**：
   - 用户分享奇葩测试结果
   - 投票选出下一个新角色
   - 举办"最毒舌AI对话"评选

2. **UGC激励**：
   - 用户可提交自己设计的"AI面试官"人设
   - 优秀作品官方采纳，署名并给予奖励

3. **IP化运营**：
   - 将"赛博上帝"等角色做成IP，推出表情包、周边
   - 联名合作（如与独立音乐人合作主题BGM）

---

## 12. 技术选型与开发排期

### 12.1 技术栈推荐（微信小程序优先）⭐

#### 方案对比

| 技术栈 | 开发周期 | 成本 | 变现能力 | 推荐度 |
|--------|----------|------|----------|--------|
| **微信小程序（原生）** | 1-2周 | 低 | ⭐⭐⭐⭐⭐ | 🏆 **MVP首选** |
| **uni-app（多端）** | 2-3周 | 中 | ⭐⭐⭐⭐ | 扩展期推荐 |
| **React H5 + 云函数** | 1周 | 低 | ⭐⭐⭐ | 备选方案 |
| **独立App（Flutter）** | 1-2月 | 高 | ⭐⭐⭐⭐⭐ | 成熟期再做 |

---

#### 推荐技术栈（微信小程序MVP）

```yaml
前端:
  平台: 微信小程序
  开发方式: 原生 WXML + WXSS + JavaScript
  UI组件: WeUI-miniprogram（官方组件库）
  状态管理: 原生 setData（简单场景够用）
  动画: WXSS Animation / Lottie动画

后端:
  架构: Serverless（云函数）
  推荐方案1: 微信云开发（适合小规模 <1000 DAU）
    - 云函数: Node.js 12/16
    - 云数据库: MongoDB
    - 云存储: 自带CDN
  推荐方案2: 第三方云函数（适合中大规模）
    - Vercel Edge Functions（推荐）
    - Cloudflare Workers
    - 阿里云函数计算
  数据库（中大规模需要）:
    - PostgreSQL 15 + Supabase（免费额度500MB）
    - Redis: Upstash（免费1万次/天）

第三方服务:
  LLM:
    - 首选：通义千问（国内合规，¥0.012/千tokens）
    - 备选：DeepSeek（便宜，¥0.001/千tokens）
    - 高质量：OpenAI GPT-3.5-turbo（¥0.015/千tokens）
  图像生成:
    - MVP阶段：预设图库（成本¥0）
    - 扩展期：通义万相 / Stable Diffusion
  对象存储:
    - 微信云存储（5GB免费）
    - 阿里云OSS（按量付费）
  内容审核:
    - 阿里云内容安全（¥1/千次）
    - 腾讯云天御（¥1.2/千次）
  广告变现:
    - 微信流量主（必接）
    - 穿山甲广告（可选，提高填充率）

部署:
  小程序托管: 微信小程序平台
  云函数部署:
    - Vercel: git push自动部署
    - 微信云开发: 微信开发者工具一键上传
  监控:
    - 微信小程序数据分析（自带）
    - Sentry（错误追踪）
```

---

#### 具体技术选型建议

**场景1：个人开发者，预算极低**
```yaml
前端: 微信小程序原生
后端: 微信云开发（完全免费，5GB存储够用）
LLM: DeepSeek（成本极低）
图像: 预设图库
总成本: <¥500/月（1000 DAU）
```

**场景2：小团队，追求性能**
```yaml
前端: 微信小程序原生
后端: Vercel云函数 + Supabase
LLM: 通义千问
图像: 预设图库 → 通义万相
总成本: <¥1,000/月（1000 DAU）
```

**场景3：创业公司，考虑多平台**
```yaml
前端: uni-app（微信+抖音小程序）
后端: 阿里云函数计算 + PostgreSQL
LLM: 通义千问 + OpenAI备用
图像: 动态生成（通义万相）
总成本: <¥3,000/月（5000 DAU）
```

---

#### 核心代码示例（微信小程序 + 云函数）

**1. 微信小程序前端调用**

```javascript
// pages/chat/chat.js
Page({
  data: {
    messages: [],
    userInput: ''
  },

  // 发送消息
  async sendMessage() {
    const userMessage = this.data.userInput;

    // 添加用户消息到界面
    this.data.messages.push({
      role: 'user',
      content: userMessage
    });
    this.setData({ messages: this.data.messages, userInput: '' });

    // 调用云函数
    wx.cloud.callFunction({
      name: 'chat',  // 云函数名称
      data: {
        sessionId: this.data.sessionId,
        message: userMessage,
        role: 'cyber_god'
      },
      success: (res) => {
        // 添加AI回复到界面
        this.data.messages.push({
          role: 'assistant',
          content: res.result.reply
        });
        this.setData({ messages: this.data.messages });
      },
      fail: (err) => {
        console.error('调用失败', err);
        wx.showToast({ title: '网络错误', icon: 'none' });
      }
    });
  }
});
```

**2. 云函数后端逻辑**

```javascript
// 云函数: cloud/functions/chat/index.js
const cloud = require('wx-server-sdk');
const axios = require('axios');

cloud.init({ env: cloud.DYNAMIC_CURRENT_ENV });
const db = cloud.database();

exports.main = async (event, context) => {
  const { sessionId, message, role } = event;

  try {
    // 1. 从数据库获取会话历史
    const session = await db.collection('sessions')
      .doc(sessionId)
      .get();

    const history = session.data.messages || [];

    // 2. 调用通义千问API
    const response = await axios.post(
      'https://dashscope.aliyuncs.com/api/v1/services/aigc/text-generation/generation',
      {
        model: 'qwen-turbo',
        input: {
          messages: [
            { role: 'system', content: getRolePrompt(role) },
            ...history,
            { role: 'user', content: message }
          ]
        },
        parameters: {
          temperature: 0.9,
          max_tokens: 200
        }
      },
      {
        headers: {
          'Authorization': `Bearer ${process.env.QWEN_API_KEY}`,
          'Content-Type': 'application/json'
        }
      }
    );

    const aiReply = response.data.output.text;

    // 3. 保存对话到数据库
    history.push(
      { role: 'user', content: message },
      { role: 'assistant', content: aiReply }
    );

    await db.collection('sessions').doc(sessionId).update({
      data: { messages: history }
    });

    // 4. 返回结果
    return { reply: aiReply };

  } catch (error) {
    console.error('云函数错误', error);
    return { error: error.message };
  }
};

// 获取角色Prompt
function getRolePrompt(role) {
  const prompts = {
    'cyber_god': '你是"赛博上帝"，一个来自2147年的超级AI...',
    // 其他角色...
  };
  return prompts[role] || prompts['cyber_god'];
}
```

---

---

### 12.2 开发排期（MVP版本）

#### 第一阶段：核心功能（2-3周）

| 任务 | 负责人 | 工作量 |
|------|--------|--------|
| 前端框架搭建 + UI设计 | 前端 | 3天 |
| 角色选择页面 | 前端 | 2天 |
| 聊天界面（含打字机效果） | 前端 | 3天 |
| 结果展示页 + 海报生成 | 前端 | 3天 |
| 后端API框架 + 数据库设计 | 后端 | 2天 |
| LLM接口封装 | 后端 | 2天 |
| Prompt工程调优 | 后端 + 产品 | 4天 |
| 会话管理逻辑 | 后端 | 2天 |
| 内容审核集成 | 后端 | 1天 |

**里程碑**：完成基础对话流程，可内部测试

---

#### 第二阶段：优化与增强（1-2周）

| 任务 | 工作量 |
|------|--------|
| 预设图库匹配算法 | 2天 |
| 分享功能（微信、朋友圈） | 2天 |
| 用户系统（登录、历史记录） | 2天 |
| 性能优化（缓存、限流） | 2天 |
| 埋点与数据统计 | 1天 |
| Bug修复与测试 | 2天 |

**里程碑**：可发布内测版本

---

#### 第三阶段：商业化与运营（持续）

| 任务 | 工作量 |
|------|--------|
| 广告系统接入 | 2天 |
| 付费功能开发 | 3天 |
| 新角色开发（每个） | 1天 |
| 运营活动页面 | 按需 |

---

### 12.3 成本预算（月度，1000 DAU规模）

```yaml
技术成本:
  服务器: ¥500 (2核4G云服务器)
  LLM API: ¥660 (1000用户 × ¥0.022/次 × 30天)
  图像生成: ¥0 (使用预设图库)
  对象存储: ¥50 (10GB)
  CDN流量: ¥100 (100GB)
  内容审核: ¥200 (按量计费)
  总计: ~¥1510/月

运营成本:
  设计师(兼职): ¥2000 (角色设计、海报模板)
  推广费用: ¥5000 (小红书投流、KOC合作)
  总计: ~¥7000/月

人力成本:
  全职开发(1人): 按实际薪资
  或兼职模式: 周末开发
```

---

### 12.4 扩展路线图

**V1.0 (MVP)**：
- 4个基础角色
- 纯文字报告 + 预设图库
- 微信小程序

**V1.5**：
- 新增2个付费角色
- 接入真实图像生成
- 支付系统

**V2.0**：
- 双人模式（情侣测试）
- 长期追踪功能（每月重测，查看变化）
- H5版本 + 独立App

**V3.0**：
- 开放平台：用户可创建自己的AI面试官
- 企业版：团队性格分析
- 多语言支持（出海）

---

## 13. 总结：从 Idea 到 Launch 的关键

### 13.1 成功的核心要素

1. **Prompt质量 > 技术复杂度**
   - 80%的精力应放在调教AI的语气和逻辑
   - 每个角色至少测试50次对话，确保稳定有趣

2. **视觉冲击力 > 功能完整性**
   - MVP阶段可以牺牲功能，但海报设计必须精美
   - Glitch风格、赛博朋克配色是差异化关键

3. **分享欲 > 测试体验**
   - 用户测完必须想发朋友圈，这是唯一的增长引擎
   - 结果要足够"有梗"、"扎心"或"惊艳"

4. **快速迭代 > 完美主义**
   - 2周内上线MVP，根据真实数据调整
   - 每周至少上线1个新角色，保持新鲜感

---

### 13.2 风险提示

- **不要过度依赖图像生成**：成本高、速度慢，MVP用预设图即可
- **不要忽视内容审核**：一次违规可能导致整个产品下架
- **不要追求技术炫技**：用户只关心结果是否有趣，不关心你用什么架构

---

### 13.3 最后的建议

这是一个**"三分技术，七分运营"**的产品。技术实现并不复杂，真正的挑战在于：

1. 如何让AI的每一句话都让人印象深刻
2. 如何让结果海报在朋友圈脱颖而出
3. 如何在新鲜感消退前建立用户习惯

**行动清单（本周就可以开始）**：

- [ ] 注册OpenAI API账号，测试GPT-3.5-turbo的角色扮演能力
- [ ] 在Midjourney生成10张"灵魂画像"风格的样图
- [ ] 手绘一版产品原型（Figma/纸笔均可）
- [ ] 找5个朋友进行"纸上原型测试"，问他们是否愿意分享结果

**记住：完成比完美更重要。先把MVP做出来，让真实用户告诉你下一步该做什么。**

---
