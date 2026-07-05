# AI工具箱 - 商业化与 SEO 配置指南

## 申请广告前必做清单

### 1. 替换占位 ID（按文件位置）

| 占位 | 文件位置 | 申请地址 |
|---|---|---|
| `G-XXXXXXXXXX` | `index.html` 的 GA4 | https://analytics.google.com/ |
| `hm.js?XXX...` | `index.html` 的百度统计 | https://tongji.baidu.com/ |
| `ca-pub-XXX...` | `index.html` 的 AdSense | https://www.google.com/adsense/ |
| `pub-XXX...` | `ads.txt` | AdSense 申请通过后自动获得 |
| 站点验证文件 | `baidu_verify-xxx.html` | https://ziyuan.baidu.com/ |

### 2. 必备文件（已自动创建）

- `sitemap.xml` — 站点地图
- `robots.txt` — 爬虫规则
- `ads.txt` — 广告商声明（AdSense 必填）
- `rss.xml` — 资讯订阅
- `weixin.png` — 微信二维码（结构化数据 logo）
- `articles.json` — 300 篇 SEO 资讯（实际在 article.html 内动态生成）

### 3. 上线前检查

- [ ] 网站 ICP 备案（中国大陆必填，否则 AdSense 国内账号会拒）
- [ ] 域名 whois 信息可公开
- [ ] 5–10 篇手工原创深度内容（AdSense 审核关键）
- [ ] 页面加载时间 < 3 秒（已通过 cdn 加速 + 单文件）
- [ ] 隐私政策页（✅ 已完成）
- [ ] 关于我们页（✅ 已完成，含联系方式）
- [ ] 站点地图提交 Google Search Console
- [ ] 站点地图提交 百度搜索资源平台
- [ ] LinkedIn / X / 知乎 至少 1 个外链

### 4. 已就位的广告位

| 位置 | 尺寸 | 期望 CPM |
|---|---|---|
| 首页头部 banner | 728×90 | $1–3 |
| 首页中部 矩形 | 300×250 | $2–5 |
| 首页原生推荐 | 自适应 | $1–4 |
| 工具合集页 banner | 728×90 | $1–3 |
| 资讯列表 每 12 篇 | 原生卡片 | $2–6 |

预估月收入（流量达到 1 万 UV/天后）：
- 横幅展示: $20–50
- 原生广告: $40–100
- 工具推广佣金（CPS）: $100–500

## 流量来源建议

1. **SEO 关键词布局**：长尾词如 "ChatGPT 写论文"、"免费 AI PPT 工具"
2. **知乎/小红书引流**：发教程类内容，链接回首页
3. **AI 工具评论文章**：每篇 800+ 字，植入工具卡片
4. **公众号 / 视频号同步**：每周更新
5. **工具收录申请**：主动联系 AI 公司，请求反向链接

## 文件结构

```
D:\zhan\
├── index.html          # 主页（已加 SEO、广告位、搜索、排行）
├── article.html        # 文章详情页
├── articles.json       # 300 篇资讯数据
├── weixin.png          # 微信二维码
├── sitemap.xml         # 站点地图
├── robots.txt          # 爬虫规则
├── ads.txt             # 广告商声明
├── rss.xml             # 资讯订阅
└── .workbuddy/         # 内存数据
```

## 关键优化点

- **JSON-LD 结构化数据**：WebSite + SearchAction + Organization + ItemList
- **Open Graph + Twitter Card**：社交分享预览
- **canonical 链接**：避免重复内容惩罚
- **点击埋点**：trackClick() 上报 GA4 事件，衡量 CTR
- **本地存储统计**：localStorage 备份点击数据，可与 GA 交叉验证
- **响应式**：3 / 2 / 1 列自适应
- **favicon 双源 + fallback**：图标始终可见
- **隐私政策 + 关于页**：AdSense 必填
