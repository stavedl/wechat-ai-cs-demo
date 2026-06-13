[English](README_EN.md) | 简体中文


# 微信群智能AI客服 — 解决方案与对话演示

通用版微信群智能AI客服的需求方案与可交互对话演示，覆盖售前、售中（以买课为例）、售后全流程，共 7 个场景：

1. 售前咨询 · 7×24 应答（含高意向线索推送销售）
2. 售中下单 · 买课全流程（选课 → 优惠券 → 催付挽单 → 成交）
3. 售后报错 · 案例库解答
4. 工单创建 · 转人工（带上下文）
5. 进度查询 · 自助服务
6. 新人入群 · 营销触达
7. 舆情预警 · 群日报

页面下方附完整需求方案：功能需求表（S/M/A/G 编号）、系统架构、实施计划、KPI、风险对策。

## 目录结构

```
.
├── index.html              # 演示主页面（加载 data/ 下的 JSON）
├── data/
│   ├── scenarios.json      # 7 个对话场景剧本（改这里换演示内容）
│   └── kb.json             # 关键词问答库、AI 名称、兜底话术
└── docs/
    ├── standalone-demo.html  # 单文件版演示（数据内嵌，双击即开，便于转发）
    └── proposal.html         # 纯文档版需求方案（无演示）
```

## 使用方式

**在线访问（推荐）**：开启 GitHub Pages 后直接访问，JSON 正常加载。

仓库 Settings → Pages → Source 选 `main` 分支根目录 → 保存，
访问 `https://<你的用户名>.github.io/<仓库名>/`

**本地预览**：`index.html` 因浏览器跨域限制不能直接双击打开，需本地起服务：

```bash
python3 -m http.server 8000
# 访问 http://localhost:8000
```

不想起服务就双击 `docs/standalone-demo.html`，效果相同。

## 自定义演示内容

- 改对话剧本：编辑 `data/scenarios.json`。每条消息格式为 `[类型, 名称, 内容]`，类型支持 `customer`（客户）、`ai`（AI客服）、`human`（人工坐席）、`sys`（系统提示）、`lead`（线索卡片）、`alert`（预警卡片）。
- 改自由问答：编辑 `data/kb.json` 的 `rules`（命中 `keywords` 任一词即回复 `reply`），`fallback` 为未命中时的兜底话术。

> 演示数据均为模拟，仅用于展示交互效果。

## 联系方式

lcl3@163.com
