[README.md](https://github.com/user-attachments/files/33200169/README.md)
# Tesla Fleet API 公钥托管

本仓库用于公开托管 Tesla Fleet API 的应用程序公钥（仅公钥，无私钥）。

## 文件结构（不要改动路径）
- `.well-known/appspecific/com.tesla.3p.public-key.pem`  ← 公钥
- `.nojekyll`  ← 防止 GitHub 忽略 .well-known 目录

## 使用方法
1. 确认仓库名是 `<你的GitHub用户名>.github.io`（例如 `kyohyde.github.io`）
2. 把本目录下的两个文件上传到仓库根目录（保持目录结构）
3. Settings -> Pages -> Source: Deploy from a branch -> main -> Save
4. 等待 1-2 分钟后验证:
   curl -H "Range: bytes=0-200" https://<用户名>.github.io/.well-known/appspecific/com.tesla.3p.public-key.pem
5. 验证通过后，开发者平台 Allowed Origin 填 https://<用户名>.github.io
