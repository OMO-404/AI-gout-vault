# AI Gout Vault

> 用 AI + Obsidian 搭建私有化痛风管理系统

不是 App，不是代码项目——是一套**模板 + Prompt + 搭建指南**。Clone 下来，让你的 AI 帮你管理痛风健康。

---

## 为什么需要这个

- 体检报告散落各处，没人帮你汇总尿酸趋势
- 痛风发作记不清诱因，无法有效预防
- 高嘌呤食物搞不清楚，每次都要查
- 商用健康 App 要上传你的隐私数据

**你只需要一套本地运行的模板，数据完全属于你自己。**

---

## 15 分钟搭建流程

```
1. Fork/Clone 本仓库
2. 用 Obsidian 打开 vault/ 文件夹
3. 填写基本信息
4. 拍体检报告 → 发给 AI → 自动提取到档案
5. 完成。以后每次复查/发作/查食物，重复第 4 步
```

---

## Claude Code 用户快速开始

如果你用 [Claude Code](https://claude.ai/claude-code)，clone 下来直接用就行：

```bash
git clone https://github.com/[你的用户名]/ai-gout-vault.git
cd ai-gout-vault
claude
# "帮我分析这份尿酸报告"（附上照片）
# "记录一次痛风发作"
# "海鲜能吃吗？"
```

`.claude/skills/` 目录下有 6 个预置技能，自动加载。

---

## 仓库结构

```
ai-gout-vault/
├── .claude/skills/               # Claude Code Skills（自动加载）
│   ├── uric-acid-extract.md      # 尿酸检验报告提取
│   ├── gout-attack-record.md     # 痛风发作记录
│   ├── gout-trend-analysis.md    # 尿酸趋势分析
│   ├── low-purine-diet.md        # 低嘌呤饮食建议
│   ├── gout-medication-guide.md  # 痛风用药指导
│   └── gout-medical-report.md    # 就医报告生成
│
├── vault/                        # Obsidian Vault 模板
│   ├── 痛风管理中心.md            # 入口 Hub
│   ├── 尿酸监测档案.md            # 尿酸追踪
│   ├── 痛风发作档案.md            # 发作记录
│   ├── tracking/                 # CSV 追踪数据
│   └── 知识库/                   # 食物、用药参考
│
├── prompts/                      # 通用 Prompt（任何 AI 都能用）
├── guides/                       # 使用指南
└── LICENSE                       # MIT License
```

---

## 技能说明

`prompts/` 里的每个文件都是独立的 Prompt，复制粘贴到任何 AI 对话里就能用：

| 技能 | 用途 | 输入 |
|------|------|------|
| 尿酸检验提取 | 提取尿酸及相关指标 | 体检报告照片 |
| 痛风发作记录 | 记录发作详情并分析 | 发作描述 |
| 尿酸趋势分析 | 分析尿酸变化趋势 | 多次检测结果 |
| 低嘌呤饮食 | 查询食物嘌呤含量 | 食物名称 |
| 痛风用药指导 | 药物信息和用药建议 | 药名或问题 |
| 就医报告生成 | 生成结构化就医报告 | 档案信息 |

---

## 谁适合用

- 想系统管理痛风健康的技术人
- 有痛风史，需要追踪尿酸和发作
- 关注饮食，需要查询嘌呤含量
- 重视隐私，不想数据上云端

---

## 谁不适合

- 不使用 AI 工具的人
- 想要一键自动化的人
- 对隐私不敏感、商用 App 就够用的人

---

## 隐私说明

所有健康数据存储在本地 Obsidian 中，不会自动上传。但当你把数据发给 AI 分析时，内容会经过 AI 服务商服务器：

- **Claude Code（API 模式）** — Anthropic 不用于模型训练
- **ChatGPT** — 建议关闭"改进模型"
- **最高隐私** — 使用本地模型（Ollama）进行分析

---

## 对比 AI Health Vault

| 特性 | AI Health Vault | AI Gout Vault |
|------|-----------------|-------------------|
| 目标用户 | 家庭健康 | 个人痛风管理 |
| 核心功能 | 通用健康 | 痛风专项 |
| 追踪重点 | 全项体检 | 尿酸、发作、饮食 |
| 知识库 | 常见指标 | 高嘌呤食物、痛风用药 |

---

## License

MIT License — 自由使用、修改、分发

---

## Author

基于 [AI Health Vault](https://github.com/runesleo/ai-health-vault) 改编
