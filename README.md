# MagicMenu

**English:** MagicMenu turns your sales data into clearer menu and dish performance — import orders, map fields once, then explore analytics and a growth checklist built for restaurant operators. Desktop app (**Tauri 2** + **Vue 3** + **TypeScript**).

**中文：** MagicMenu 面向餐饮经营者，把订单数据变成可看的菜单与菜品表现：导入销售明细、完成字段与主食配置后，即可进行菜单/菜品分析与增长执行清单。桌面客户端（**Tauri 2** + **Vue 3** + **TypeScript**）。

---

## Download & install | 下载与安装

- **Installers** are published via **GitHub Releases** (or your chosen distribution channel). Download the latest `.exe` / installer for Windows from the release page.
- **系统要求（参考）：** Windows 10/11（以实际发布说明为准）；建议 1280×800 及以上分辨率。

若此仓库为「仅发布安装包、不含源码」的公开仓库，请将 **Releases** 链接写在此处，例如：  
`https://github.com/<org-or-user>/<repo>/releases`

---

## Quick start | 快速上手

1. **Import data** — CSV or Excel (first worksheet). Optional: connect **Square / Shopify** from the desktop app when configured (developer setup).
2. **Analysis setup** — Map each logical field to a column; select at least one **staple / traffic-anchor** category.
3. **Menu analytics** — Compare time windows, category metrics, and attach rates.
4. **Dish analytics** — Dish-level views and quadrant charts (when data supports them).
5. **Growth plan** — Checklist for signature-dish execution and follow-up.

界面支持 **简体中文** 与 **English**（可在应用内切换语言）。

---

## Privacy | 隐私说明

- 分析以**本地客户端**为主：导入文件与会话状态主要用于在本机完成计算与展示；不向 MagicMenu 服务器上传完整订单明细（除非你在独立版本另行接入了云同步或埋点，请以打包协议为准）。
- POS 直连 OAuth 仅在**桌面端**发起；回调与密钥配置见开发者文档。

---

## Contact | 联系方式

应用内 **关于 / Contact the author** 页面提供作者联系信息与邮件说明。

---

## Proprietary notice | 著作权说明

本软件为专有作品；**未随安装包提供源代码授权**时，请勿逆向、再分发安装包以外的声称「开源」的版本。第三方开源组件的权利义务以其各自许可证为准（见各依赖项声明）。

---

## For developers | 开发者文档

工程根目录即 **前端 + Tauri/Rust 壳**；详细路由、导入规格与发布清单见 `docs/`。

### Dev | 开发

```bash
npm install
npm run tauri dev
```

仅前端（无桌面壳）：`npm run dev`

### Main routes | 主要路由

- `/` — Home（数据源选择、导入、继续上次）
- `/import` — 文件导入预览
- `/mapping` — 分析设置（字段映射、主食品类）
- `/menu` — 菜单分析
- `/dishes` — 菜品分析
- `/reports` — 增长计划 / 清单
- `/mvp-week` — 关于（About / 联系作者入口）

### Square / Shopify（桌面 OAuth）

默认可能**不向终端用户展示**首页 POS 入口（依赖开发者凭据）。内部测试：根目录 `.env.local` 设置 **`VITE_MAGICMENU_SHOW_POS=1`** 并重启 Vite。环境变量示例见 **`.env.example`**；商户对接说明见 **[`docs/MERCHANT_POS_SETUP.md`](./docs/MERCHANT_POS_SETUP.md)**。

**Square：** OAuth 重定向 URL 须与默认 **`http://localhost:8745/callback`** 完全一致（`localhost` 与 `127.0.0.1` 视为不同主机）。端口 `MAGICMENU_OAUTH_PORT`；主机 `MAGICMENU_OAUTH_REDIRECT_HOST`。

**Shopify：** 应用后台允许的重定向 URL 同上；配置 **`SHOPIFY_CLIENT_ID`**、**`SHOPIFY_CLIENT_SECRET`**。

### Tech notes | 技术要点

- 导入预览：Papa Parse；会话可经 **IndexedDB**（`magicmenu_session`）恢复。
- 菜单分析：锚点日、多档窗口、搭售与结构指标等见 `docs/menu-analysis-metrics.md`、`docs/import-spec.md`。
- **v1.0 发布清单：** [`docs/V1.0_RELEASE_CHECKLIST.md`](./docs/V1.0_RELEASE_CHECKLIST.md)

### Build | 构建

```bash
npm run build
```

桌面安装包：`npm run tauri build`（需已安装 Rust / Tauri 工具链；详见 Tauri 文档）。

### Repository layout | 目录

| Path | Description |
|------|-------------|
| `src/` | Vue 前端 |
| `src-tauri/` | Tauri / Rust |
| `docs/` | 产品与工程规格 |
| `scripts/` | 辅助脚本 |
| `samples/demo_orders_qty_amount_1.csv` | 小样本演示 |

更多链接见原索引：**产品口径 / 导入 / 文案：** [`docs/product-decisions.md`](./docs/product-decisions.md)、[`docs/import-spec.md`](./docs/import-spec.md)、[`docs/ui-copy-mvp.md`](./docs/ui-copy-mvp.md)；**报表进展 PRD：** [`docs/reports-progress/PRD-MVP.md`](./docs/reports-progress/PRD-MVP.md)。

---

**Product identifier（Tauri）：** `com.magicmenu.app` · **当前版本（package）：** `0.1.0` — 发布时请与 **GitHub Release tag** 及安装包版本号对齐。
