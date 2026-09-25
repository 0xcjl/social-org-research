# social-org-research（社会创新 / 共益企业调研技能）

> 调研 B 型企业 / 共益企业 / 社会企业 / NGO / 青年文化品牌——一套带 10 个信息维度、`quick | deep` 深度切换开关、并附有已验证真实案例的研究提示词框架。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Skill](https://img.shields.io/badge/type-agent%20skill-blueviolet)](./SKILL.md)
[![Platforms](https://img.shields.io/badge/platforms-Hermes%20%7C%20Claude%20Code%20%7C%20OpenClaw-lightgrey)](#平台兼容)
[![Version](https://img.shields.io/badge/version-0.1.0-success)](./CHANGELOG.md)

> **[English](./README.md)** | 简体中文（你在这里）

---

## 这是什么

`social-org-research` 是一个针对**社会创新组织**的结构化研究提示词 + 评估框架——B Corp、社会企业、NGO、公共利益平台、青年文化品牌,以及所有"商业向善"实体。

跟通用市场调研不同,本技能专门研究**收入与使命混合**的组织：内容赞助、捐赠人关系、志愿者劳动、跟国际 NGO 的付费合作、政府专项、以及"联合出品"而非"赞助"的品牌关系。

附 **10 个信息维度**、**`depth: quick | deep` 切换开关**、以及一份来自真实 BottleDream 调研案例的展示文档。

---

## 为什么用它

| 没有 `social-org-research` | 有 `social-org-research` |
|------------------------------|------------------------------|
| "这 NGO 怎么赚钱?" → 一头雾水 | 给出具体收入类目：媒体 / 内容赞助 / 培训 / 咨询 / 联名产品 / 活动赞助 |
| "志愿者给钱吗?" → 套中国公益刻板印象瞎猜 | 引用《志愿服务条例》+ 5 个非现金钩子框架 |
| "联合出品方 vs 赞助商有啥区别?" → 分不清 | 清晰分类：联合出品方 = 自带方案 + 资源 + 产品解题;赞助商 = 付钱挂名 |
| "注册资本 100 万,这公司是不是很小?" | 区分：注册资本 ≠ 实际规模;交叉验证 LinkedIn / B Lab / 办公空间 |

---

## 适用场景

| 场景 | 用本技能? |
|------|-----------|
| 调研 B Corp、社会企业、共益公司 | ✅ 是 |
| 调研 NGO、公共利益平台、基金会 | ✅ 是 |
| 梳理青年文化品牌的内容 + 活动 + 社群运营 | ✅ 是 |
| 想搞清楚"商业向善"组织靠什么活 | ✅ 是 |
| Pitch 会议前的快速扫描 | ✅ 是（`depth: quick`） |
| 调研商业产品或 B2B SaaS 公司 | ❌ 用 `market-research` 替代 |
| 学术论文文献综述 | ❌ 用 `academic-research` 替代 |
| 跨多家做行业趋势研究 | ❌ 用 `deep-research` 替代 |

---

## 触发关键词

**英文：** `social enterprise`, `B Corp`, `co-benefit`, `co-benefit enterprise`, `social innovation`, `NGO research`, `youth culture brand`, `public-interest platform`, `B Impact Assessment`, `BIA score`, `social good`, `volunteer benefits`, `co-creator vs sponsor`

**中文：** 调研 NGO / 共益企业 / 社会企业 / 公益平台 / B 型企业 / 青年文化品牌 / 商业向善 / 创变者 / 志愿者报酬 / 影响力投资 / 公益基金会 / 共创伙伴 / 社会创新企业

---

## 快速开始

### 1. 安装（Hermes / OpenClaw）

```bash
hermes skills install 0xcjl/social-org-research
# 或从本地源码软链
ln -s ~/.hermes/skills/social-org-research ~/.openclaw/workspace/skills/social-org-research
```

### 2. 使用

在任何 agent 对话中触发：

```
调研 BottleDream,depth: deep
```

技能会自动加载,跑完 10 个维度,产出 Markdown + 带可点击链接的 PDF。

---

## 案例：`depth: deep` 一次产出什么

一次真实 BottleDream 调研（详见 [`references/case-bottledream.md`](./references/case-bottledream.md)）产出：

- **18 页 A4 PDF**（`bottledream-research.pdf`,~2.35 MB）,35 个来源链接渲染为可点击 `/Link` 注释
- **VBC 验证** `md_links = matched_links = 35`（100% 匹配）
- **35 个来源** 覆盖 B Lab / LinkedIn / 36氪 / 新浪财经 / 网易 / 中国发展简报 / WonderCV / 人民网 / 达沃斯 / Journal of Futures Studies 等
- **三轮递进深挖** 回答用户关于活动执行和志愿者报酬的追问

没有本技能,同样的深度需要 ~15 小时人工研究,而且容易漏掉"志愿者无现金报酬但免费午餐 + 免费 T 恤 + 免费沉浸体验"这类关键事实。

---

## 目录结构

```
social-org-research/
├── SKILL.md                      # 技能主体（由 agent 加载）
├── README.md                     # 英文 README
├── README.zh-CN.md               # 本文件
├── INSTALLATION.md               # Hermes / OpenClaw / Claude Code 安装指南
├── LICENSE                       # MIT
├── CHANGELOG.md                  # 版本历史
├── .gitignore
└── references/
    └── case-bottledream.md       # 真实案例（简化版）
```

---

## 自定义

针对特定细分领域（气候技术 NGO、基金会、特定地区的社会企业）改造：

1. **调整 SKILL.md §"信息源优先级" 表**——加地区或行业特定数据库
2. **增删 10 个维度**——如果目标行业强调其他东西（如医疗 NGO 加"监管文件"维度）
3. **追加新 Pitfall**——真实研究中遇到就加到 §"关键 Pitfalls"
4. **更新 Use Cases 路由表**——某些场景需要重定向到别的技能

---

## 故障排查

| 问题 | 解决 |
|------|------|
| `gh auth status` 失败 | `gh auth login` |
| `clawhub publish` 报 YAML 错误 | 跑 `python3 -c "import yaml; yaml.safe_load(open('SKILL.md').read().split('---')[1])"` 验证 frontmatter |
| Topics 数量 ≠ 13 | 重跑 `gh repo edit --add-topic` 每个缺失的 tag |
| README 不渲染 | 本地用 `grip -b README.md` 预览 |
| 技能加载但 description 触发不对 | 编辑 frontmatter `description`（≤60 字符,避免索引截断） |

---

## 平台兼容

| 平台 | 兼容? | 备注 |
|------|-------|------|
| Hermes | ✅ | `~/.hermes/skills/social-org-research/` |
| OpenClaw / Claude Code | ✅ | 软链到 `~/.openclaw/workspace/skills/social-org-research/` |
| 其他 SKILL.md 阅读器 | ✅ | 标准 YAML frontmatter + markdown body |

---

## 致谢

- **作者：** 0xcjl
- **License：** MIT
- **案例来源：** 作者本人用本技能做的真实 BottleDream 调研,2026 年 9 月
- **发布技能：** `agent-skill-publisher`（Hermes 内部）—— 9 步端到端发布流程

---

## License

MIT © 2026 0xcjl
