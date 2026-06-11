# TrailQuest · 智能旅游行程规划

> 多页面互动旅游行程规划平台 · 高德地图驱动 · Stripe 风格设计

## 功能

- **🏠 首页** — 目的地搜索 · 热门路线推荐 · 分类浏览
- **🗺️ 行程规划** — Day Tab 切换 · 时间轴卡片 · 地图联动 · 交通规划 · POI 分类配色
- **🔥 热门路线** — 10 条经典路线模板 · 多维度筛选 · 一键套用
- **📍 周边探索** — POI 搜索 · 周边雷达 · 分类筛选 · 地图标注
- **🤖 智能问答** — FAQ 本地秒回 · 外部大模型 API 配置 · 旅行问答补充
- **📊 仪表盘** — POI 分布 · 预算分析 · 每日概览 · 数据可视化
- **💾 我的行程** — 保存/查看/删除 · localStorage 持久化

## 技术栈

- 高德地图 JS API 2.0（AutoComplete / PlaceSearch / Geocoder / Driving / Walking / Weather）
- 原生 HTML/CSS/JS，零依赖框架
- GitHub Pages 自动部署
- Stripe 风格青蓝渐变 Banner + 玻璃拟态徽章
- 外部大模型接口兼容 OpenAI Chat Completions，由用户在页面本机配置 Base URL / Model / API Key

## 路线与数据

当前可直接打开完整行程详情的路线包括：成都、西安、北京、重庆、杭州、大理。热门路线页只保留这些已有完整 POI 数据的城市，避免出现卡片可点但详情页缺失的断点。

推荐路线参考携程旅游攻略、马蜂窝自由行攻略、高德地图 POI/路线信息及常见城市经典玩法，并在前端重新编排为可执行的地图点位和时间轴。

## 问答配置

`qa.html` 默认先匹配本地 FAQ。若需要调用外部大模型，在页面右侧配置：

- Base URL：兼容 OpenAI Chat Completions 的接口地址
- Model：模型名称
- API Key：仅保存到当前浏览器 `localStorage`

生产环境不建议把 API Key 直接暴露在前端，应通过后端代理转发。

## 部署

Push 到 GitHub `main` 分支后，GitHub Actions 自动部署到 Pages。
