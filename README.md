# Hangzhou Jianqiao Airport Noise Corridor Map / 杭州笕桥机场噪声风险走廊图

[中文说明](#中文说明) · [English](#english) ·
[Live site](https://myshkin451.github.io/hangzhou-jianqiao-noise-corridor/)

> A bilingual public-interest map for people renting or buying homes in Hangzhou.
> It helps screen possible aircraft-noise exposure around Jianqiao Airport using
> public information, transparent assumptions, and on-site verification advice.

> 一个面向杭州租房、买房和新来杭州人群的双语公益小工具：用公开资料、
> 透明假设和实地核验清单，初筛笕桥机场周边可能的训练噪声影响。

## 中文说明

### 这是什么

这是一个纯静态、可公开访问的交互地图，用来帮助普通人在看房前快速判断某个
小区、地铁站或片区是否可能处在笕桥机场训练噪声的重点影响走廊附近。

它适合回答这些问题：

- 我想租/买的地方离推断走廊中心线有多远？
- 这个片区初筛上属于红色、橙色、黄色还是外围？
- 如果我仍然喜欢这套房，实地要怎么听、怎么问、怎么验证？
- 不懂中文的外国朋友来杭州前，能不能先看懂风险？

### 主要功能

- 中英双语界面，支持手动切换。
- 点击地图任意位置即可评估风险。
- 搜索小区、片区或地铁站并显示候选结果。
- 支持当前位置评估，必须由用户主动授权。
- 支持复制带语言、风险口径和点位的分享链接。
- 支持标准地图、浅色地图和卫星影像底图切换。
- 内置重点片区速览和实地核验清单。
- 附带方法、来源、隐私和限制说明。

### 它不是什么

- 不是官方航线图。
- 不是军方、政府、法律、工程或声学报告。
- 不是噪声环评分贝线。
- 不能替代多次实地蹲点和邻里访谈。

军用机场不会公开精确航线、训练时间或实时轨迹，所以这个项目只把公开信息
转化成“看房初筛模型”。它的价值在于提醒风险，不在于给出权威结论。

### 地图底图选择

当前默认使用 OpenStreetMap 标准底图，因为它无需 API key，适合公共静态站点。
同时保留 CARTO 浅色地图，方便看清红橙黄走廊；新增 Esri World Imagery 卫星影像，
方便用户观察真实地物、河道、道路和居住区边界。

如果未来希望进一步提升中文 POI、英文标签、卫星新鲜度和中国大陆访问稳定性，
可以考虑 MapTiler 或 Mapbox 这类商业服务；但它们通常需要 API key、账户配置和
用量管理。高德/百度在中国大陆 POI 更强，但使用 GCJ-02 坐标系，和本项目当前
WGS84/OSM/Leaflet 模型混用时需要额外坐标转换，不能直接替换。

### 中国大陆访问

`github.io` 在中国大陆不属于可保证稳定访问的发布渠道。它可能能打开，也可能因
网络、DNS、CDN 或地区运营商差异而变慢或不可访问。这个仓库适合作为公开首发和
版本管理；如果需要面向大陆用户长期稳定传播，后续建议迁移或镜像到自己的域名。

迁移很简单：本项目是纯静态文件，不绑定 GitHub Pages。未来个人网站做好后，可以：

- 把 `index.html` 放进个人平台的某个路由，例如 `/tools/jianqiao-noise/`；
- 或给 GitHub Pages 配置自定义域名；
- 或部署到 Cloudflare Pages、Vercel、Netlify、对象存储/CDN 等静态托管。

如果使用中国大陆服务器或大陆 CDN，通常需要考虑 ICP 备案。

### GitHub Pages 是否免费

对公开仓库来说，GitHub Free 支持 GitHub Pages。这个项目目前没有后端、没有数据库、
没有构建服务依赖，日常运行不会产生服务器费用。需要注意 GitHub Pages 有使用限制，
例如官方文档列出的软带宽限制；它不适合当作大流量商业网站或 SaaS 托管。

### 关键词

杭州笕桥机场、笕桥机场噪音、杭州飞机噪音、杭州买房、杭州租房、机场噪声、
Jianqiao Airport, Hangzhou airport noise, Hangzhou housing, aircraft noise,
noise corridor map, bilingual map, OpenStreetMap, Leaflet, satellite imagery.

## English

### What This Is

This is a static, bilingual screening map for people renting or buying homes in
Hangzhou. It helps users understand whether a neighborhood, compound, or metro
station may be close to an inferred aircraft-noise exposure corridor around
Jianqiao Airport.

It is designed for practical questions:

- How far is this location from the inferred corridor centerline?
- Is this area red, orange, yellow, or outside the main model?
- What should I listen for before signing a lease or buying a home?
- Can non-Chinese-speaking residents understand the risk before moving to
  Hangzhou?

### Features

- Chinese and English interface.
- Click any map location to rate it.
- Search for compounds, areas, or metro stations.
- Opt-in browser geolocation.
- Shareable links with language, risk model, and selected point.
- Standard, light, and satellite basemap switching.
- Area quick scan and on-site listening checklist.
- Transparent method, source, privacy, and limitation notes.

### What This Is Not

- Not an official flight path.
- Not a military, government, legal, engineering, or acoustic assessment.
- Not a decibel contour map.
- Not a substitute for repeated on-site listening.

Military airfields do not publish exact routes, training schedules, or real-time
tracks. This project turns public information into a practical screening model,
not an authoritative map.

### Basemap Rationale

The default map uses OpenStreetMap because it requires no API key and works well
for a public static site. CARTO light tiles make the risk corridor easier to
read, and Esri World Imagery adds a satellite view for checking real geography,
roads, rivers, and residential boundaries.

For stronger multilingual labels, fresher commercial imagery, and managed
traffic, MapTiler or Mapbox could be added later, but they require API keys and
usage management. Mainland Chinese providers such as AMap or Baidu have stronger
local POI coverage, but they use GCJ-02 coordinates; mixing them directly with
the current WGS84/OSM/Leaflet model would create alignment errors unless
coordinate conversion is added.

### Access From Mainland China

`github.io` is not a guaranteed stable delivery channel in mainland China. It may
work for some users and fail or load slowly for others depending on network,
DNS, CDN route, and ISP behavior. The GitHub Pages version is a good public
prototype and source-of-truth repository; for long-term mainland distribution,
mirror or migrate the static files to a custom domain or another static host.

Migration is straightforward because this project is plain HTML/CSS/JS:

- move `index.html` into a route on the future personal website;
- configure a custom domain for GitHub Pages;
- deploy the same files to Cloudflare Pages, Vercel, Netlify, object storage, or
  another CDN-backed static host.

Mainland China hosting or CDN usage usually requires checking ICP filing
requirements.

### Cost

GitHub Pages is available for public repositories on GitHub Free. This project
has no backend, database, build system, or server-side runtime, so there is no
ordinary hosting bill. GitHub Pages still has usage limits, including soft
bandwidth limits, and should not be treated as unlimited commercial hosting.

## Sources

- Hangzhou public complaint record:
  <https://yst.hangzhou.com.cn/question.php?question_id=181113171468>
- Article mentioning Jianqiao runway dimensions:
  <https://www.cgejournal.com/article/id/9496>
- OpenStreetMap tile usage policy:
  <https://operations.osmfoundation.org/policies/tiles/>
- OpenStreetMap copyright:
  <https://www.openstreetmap.org/copyright>
- Nominatim usage policy:
  <https://operations.osmfoundation.org/policies/nominatim/>
- Esri World Imagery attribution guidance:
  <https://support.esri.com/en-us/knowledge-base/what-is-the-correct-way-to-cite-an-arcgis-online-basema-000012040>
- GitHub Pages limits:
  <https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits>
- GitHub Pages custom domains:
  <https://docs.github.com/articles/using-a-custom-domain-with-github-pages>

## Privacy

Searches are sent directly from the browser to Nominatim only after the user
submits a query. The geolocation button only runs after the user clicks it and
grants browser permission. This static page has no server-side collection layer.

Users should avoid entering names, phone numbers, room numbers, or other private
information into the search box.

## Files

- `index.html` - the complete static app.
- `.nojekyll` - tells GitHub Pages to publish static files directly.
- `robots.txt` and `sitemap.xml` - basic search-engine discoverability.
- `NOTICE.md` - source, attribution, and limitation notices.
- `LICENSE` - MIT license for the code.

## Local Preview

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Open:

<http://127.0.0.1:8765/>

## Publish With GitHub Pages

The current repository publishes from the `main` branch root.

```bash
gh api --method PUT /repos/myshkin451/hangzhou-jianqiao-noise-corridor/pages -f 'source[branch]=main' -f 'source[path]=/'
```
