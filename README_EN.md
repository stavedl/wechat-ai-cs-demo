# WeChat Group AI Customer Service — Solution & Interactive Demo

A general-purpose WeChat group AI customer service solution with an interactive conversation demo, covering pre-sales, in-sales, and after-sales workflows across 7 scenarios:

1. Pre-sales Consultation · 7×24 auto-response (with high-intent lead push to sales)
2. Order Flow · Full course purchase journey (browse → coupon → cart recovery → conversion)
3. After-sales Error Handling · Knowledge base-powered troubleshooting
4. Ticket Creation · Escalation to human agent (with full context handoff)
5. Progress Inquiry · Self-service query
6. New Member Welcome · Marketing outreach
7. Sentiment Alert · Daily group operations report

The page also includes a full solution document: feature requirements (S/M/A/G IDs), system architecture, implementation plan, KPIs, and risk mitigation.

## File Structure

```
.
├── index.html              # Main demo page (data embedded, open by double-click)
├── data/
│   ├── scenarios.json      # 7 conversation scripts (edit here to customize demo)
│   └── kb.json             # Keyword Q&A rules, AI name, fallback response
└── docs/
    ├── standalone-demo.html  # Single-file demo (data inline, easy to share)
    └── proposal.html         # Solution document only (no demo)
```

## Live Demo

GitHub Pages: **https://stavedl.github.io/wechat-ai-cs-demo/**

## Usage

**Online (recommended):** Enable GitHub Pages and visit the link above. JSON loads normally.

Repo Settings → Pages → Source: `main` branch root → Save.

**Local preview:** `index.html` can be opened by double-clicking directly — data is embedded and no local server is needed.

If you prefer a server:

```bash
python3 -m http.server 8000
# Visit http://localhost:8000
```

## Customization

- **Edit conversation scripts:** Modify `data/scenarios.json`. Each message format: `[type, name, content]`. Supported types: `customer`, `ai`, `human`, `sys`, `lead`, `alert`.
- **Edit free-input Q&A:** Modify `data/kb.json`. Each rule matches any keyword in `keywords` and returns `reply`. `fallback` is used when no rule matches.

> All demo data is simulated and for display purposes only.

## Contact

lcl3@163.com
