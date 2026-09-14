# 2026 宜蘭縣長選舉對照

林國漳與吳宗憲的基本介紹、主要政見與爭議對照。單一靜態頁面（`index.html`），資料截至 2026-09-14，內容整理自公開報導。

## 部署

| 平台 | 方式 |
|---|---|
| GitHub Pages | 由 `main` 分支根目錄直接發布 |
| Cloudflare Pages | 每次 push 到 `main` 時，由 GitHub Actions（`.github/workflows/cloudflare-pages.yml`）自動部署 |

### Cloudflare Pages 首次設定

在 GitHub repo 的 **Settings → Secrets and variables → Actions** 新增兩個 secret：

- `CLOUDFLARE_ACCOUNT_ID`：Cloudflare 儀表板右側欄的 Account ID
- `CLOUDFLARE_API_TOKEN`：在 Cloudflare **My Profile → API Tokens** 建立，權限選 **Account → Cloudflare Pages → Edit**

設定好之後，到 **Actions → Deploy to Cloudflare Pages → Run workflow** 手動跑一次；之後每次 push 都會自動部署。未設定 secret 時，這個 workflow 會略過部署，不會報錯。
