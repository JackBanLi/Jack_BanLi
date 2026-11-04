# 冯瑞 · 游戏动画作品集 2026.10

《Jack_BanLi》角色动画短片作品集网页。

- 在线观看：扫描页面内二维码，或直接打开 GitHub Pages 网址
- 视频：`video.mp4`（1280×720 / 30fps / 约 16MB，H.264 + AAC，已开启 faststart）
- 封面：`cover.jpg`
- 页面：`index.html`（纯静态，无外部依赖）

## 说明

为了让手机扫码后能流畅播放，仓库内存放的是压缩后的网络版视频；
**原始视频（85.7MB，9Mbps）保留在本地 `D:\A1fr\作品集\11.4作品集\Jack_BanLi.mp4`，未做任何修改。**

## 如何更新视频

1. 用 ffmpeg 压缩新视频：

   ```bash
   ffmpeg -i 原视频.mp4 -c:v libx264 -preset slow -crf 20 \
     -pix_fmt yuv420p -c:a aac -b:a 128k -movflags +faststart video.mp4
   ```

2. 替换本目录的 `video.mp4`，提交并推送即可，GitHub Pages 会自动更新。

> GitHub 单文件上限 100MB；超过则无法直接推送，建议保持压缩版在 20MB 以内。
