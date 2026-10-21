# 深海游乐场

wefcdse 的个人主页 / 小游戏合集，部署在 <https://wefcdse.github.io/>。

单文件 `index.html`，无依赖、无构建，双击或起本地服务即可预览：

```powershell
python -m http.server 8000
```

## 部署

首次发布：

1. 在 GitHub 新建 **public** 仓库 `wefcdse.github.io`。
2. 在本目录：

   ```powershell
   git init -b main
   git add .
   git commit -m "Add homepage"
   git remote add origin https://github.com/wefcdse/wefcdse.github.io.git
   git push -u origin main
   ```

3. 仓库 **Settings → Pages → Source** 选 **GitHub Actions**，工作流跑完即上线。

## 添加新游戏

游戏部署在 `https://wefcdse.github.io/<仓库名>/`。在 `index.html` 里复制 `a.card` 那一块，改掉：

- `href`：`/<仓库名>/`
- 缩略图 SVG（顺手改改鱼群位置）
- 标题、描述、`tags`
- `.section-head` 里的数量（当前 `01 TITLE`）

`card.soon`（虚线占位卡）可以保留在最后，也可以删掉。

## 已有游戏

| 游戏 | 链接 | 说明 |
| --- | --- | --- |
| 鱼群模拟 | `/fish-school/` | Rust + WASM 的 Boids 鱼群 |
