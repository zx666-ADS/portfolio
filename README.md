# 钟鑫 · AI 短视频制作人 作品集

一个零依赖的纯静态作品集网站。可直接拖到 Netlify 发布，也可用任意静态托管（GitHub Pages、Vercel、自有服务器）。

## 目录结构

```
portfolio/
├── index.html        # 首页：Hero 定位 + 能力矩阵 + 4 支成片播放器 + 简历项目 + 联系方式
├── workflows.html     # 作品流程文档：4 支成片的完整制作全流程（8 步管线 + 技术栈 + 交付物）
├── media/             # 视频资源
│   ├── fitness_40s.mp4   # 健身 Vlog 40s（9:16 竖屏）
│   ├── coffee_40s.mp4    # 咖啡馆手冲 Vlog 40s（9:16 竖屏）
│   ├── monster_15s.mp4   # 魔爪饮料 15s 电视广告（16:9）
│   └── wukong_30s.mp4    # 孙悟空大闹天宫 30s 电影感（16:9）
└── README.md          # 本文件
```

## 部署到 Netlify（拖放法，无需命令）

1. 打开 https://app.netlify.com/drop
2. 把整个 `portfolio` 文件夹拖进去
3. 等待几秒，Netlify 自动给出公开链接（形如 `https://xxx.netlify.app`）
4. 要换域名：在 Netlify 控制台 Domain settings 里绑定自己的域名

## 其他托管方式

- **GitHub Pages**：把本目录推到仓库，仓库 Settings → Pages → 选分支根目录。
- **Vercel**：`vercel deploy` 指向本目录即可。
- **自有服务器**：把文件上传到任意支持静态文件的目录，`index.html` 设为入口。

## 本地预览

直接用浏览器打开 `index.html` 即可。若浏览器限制本地视频加载，可在目录下起一个静态服务：

```
python -m http.server 8080
```

然后访问 http://localhost:8080

## 如何自定义

- **换视频**：把新 mp4 放进 `media/`，修改 `index.html` 里对应的 `<video src="media/xxx.mp4">`。竖屏视频加 `class="vert"`（卡面 16:9 预览、全屏 9:16 完整显示）。
- **改文案/联系方式**：编辑 `index.html`，搜索「钟鑫」「13247533068」「ZxsDsG03」直接替换。
- **改流程文档**：编辑 `workflows.html`。

## 注意事项

- 视频文件较大（约 100MB），托管平台对单仓库/单站点体积可能有上限，注意各平台免费额度。
- 所有作品均由 AI 工具辅助生产，流程细节见 `workflows.html`。
