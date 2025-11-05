---
applyTo: '**'
---
# Instructions for Editing Text in HTML Files
When editing text content in HTML files, please follow these guidelines to ensure clarity and consistency:
1. Using bootstrap and jquery CDN links as in the template file.
2. After making changes, update the README.md file to reflect the changes made in the HTML files. Adding update date after each edited file is recommended.
3. 在生成含影片的網頁時，請採用以滾動控制影片播放的設計。影片必須在 loadedmetadata 完成後才能設定 currentTime，並使用 requestAnimationFrame 搭配滾動事件來更新播放進度，避免跳動與卡頓。同時加入時間差門檻以減少過度更新，並確保影片為 muted 並支援 playsinline，使不同裝置上都能平順播放。
