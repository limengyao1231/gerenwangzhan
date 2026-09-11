# 李梦垚个人网站

基于 React + Vite 的个人网站，推荐部署到 Cloudflare Pages。

## 本地运行

```bash
pnpm install
pnpm dev
```

访问 `http://127.0.0.1:5173/`。

## Cloudflare Pages 部署

1. 将项目上传到 GitHub。
2. 登录 Cloudflare，进入 `Workers & Pages`。
3. 选择 `Create application > Pages > Connect to Git`。
4. 选择 GitHub 仓库。
5. 构建配置：
   - Framework preset: `Vite`
   - Build command: `pnpm build`
   - Build output directory: `dist`
   - Root directory: `/`
6. 部署完成后，进入项目 `Custom domains`。
7. 添加 `www.lmy1231.com` 和 `lmy1231.com`。
8. 如果域名 DNS 已托管在 Cloudflare，自定义域名会自动配置。
9. 在 `SSL/TLS` 中开启 `Full (strict)` 和 `Always Use HTTPS`。