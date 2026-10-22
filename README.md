# AI 全景知识图谱 · 交互式浏览

个人长期维护的 AI 领域全景知识图谱，只读浏览站点。当前 **10,025 节点 / 34,354 边**，覆盖 AI 技术、产业、人物、时间线、地域、政策等 20 类实体与关联、时间线、参与、衍生、竞争、合作、并购、投资等关系。

## 在线浏览

- **2D 全功能视图**：[web/index.html](web/index.html) —— WebGL 全图单画布：搜索定位、节点详情（含一手来源链接）、按实体类型/关系类型/维度/年份筛选、两实体最短关系路径。
- **3D 星系视图**：[web/graph3d.html](web/graph3d.html) —— 展示用。

## 数据

- `graph_data.json` 为唯一数据源，**每周增量生长**（新闻保鲜扫描 + 双钥裁决合并）。
- 节点字段：`id` / `name` / `type`（20 类）/ `desc` / `dim` / `year` / `link`（部分实体另有 `url` 字段，等价来源）。
- 边字段：`source` / `target` / `type` / `desc`。

## 数据纪律

0 捏造：无权威来源不建节点、不编 URL；链接均为一手来源（arXiv / 交易所公告 / 官方站点 / 部委文件）。

## 本地运行

```bash
git clone https://github.com/wenize/ai-panorama-graph.git
cd ai-panorama-graph
python -m http.server 8973
# 浏览器打开 http://127.0.0.1:8973/web/index.html
```

引擎：graphology + sigma.js（2D WebGL2）+ 3d-force-graph，依赖已本地化，无 CDN 依赖。

## 免责

个人学习与研究整理，信息以节点附带的来源链接为准；数据每日/每周仍在生长，欢迎按 schema 自取使用。
