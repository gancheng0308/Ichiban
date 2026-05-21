# 一番赏系统（Ichiban）

基于设计稿落地了可运行的前端静态原型（HTML/CSS），包含：

- 用户端首页（抽赏卡片、功能入口、底部导航）
- 抽赏详情页（奖池概率、抽一次/十次按钮）
- 管理后台仪表盘（指标卡、活动表格）

## 本地运行

```bash
python3 -m http.server 8080
# 访问 http://localhost:8080/web/
```

## GitHub Pages 自动部署

仓库已内置 GitHub Actions 工作流：`.github/workflows/deploy-pages.yml`。

### 1) 推送到 GitHub 仓库
确保仓库有远程地址并推送到 `main` 分支：

```bash
git remote add origin <你的仓库地址>
git branch -M main
git push -u origin main
```

### 2) 开启 Pages
在 GitHub 仓库页面：

- `Settings` → `Pages`
- `Build and deployment` 选择 `Source: GitHub Actions`

### 3) 等待部署完成
首次部署完成后，站点链接通常是：

- `https://<你的GitHub用户名>.github.io/<仓库名>/`

本项目部署目录为 `docs/`，入口文件为 `docs/index.html`。

## 下一步建议

1. 接入 Vue/React 并拆分组件
2. 对接后端 API（活动、奖品、订单、用户）
3. 增加抽奖动画、支付流程、订单流转
4. 实现 RBAC 权限与管理后台操作日志
