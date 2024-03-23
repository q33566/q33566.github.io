---
title: 網站部屬紀錄(hexo + gitpage)
date: 2024-03-23 15:06:08
tags:
---
## 部屬流程
- step1
    - 在github上新增Repository，取名為: `使用者名稱.github.io`
- step2 
    - 在本地端，找到hexo專案資料夾中的_config.fluid.yml，並將`# Deployment`部分改為
    ```
    deploy:
    type: git
    repo: https://github.com/使用者名稱/使用者名稱.github.io.git
    branch: gh-pages
    ``` 
    
- step3
    - 在終端機，本地端hexo專案資料夾底下輸入以下指令
    ```
    npm install hexo-deployer-git --save
    hexo c
    hexo g
    hexo d
    # 之後的網站更新我也是輸入這3個
    ```
這時候到`https://使用者名稱.github.io/`查看，發現部屬成功。<br>
最後，我在同一個Repository裡面建立了backUp分支用來存程式碼。

## 參考資料
<a href=https://ithelp.ithome.com.tw/articles/10272520>1. Day 11：將你的 Hexo 部落格部屬到 Github Pages</a>
<br>
<a href=https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site>2. Configuring a publishing source for your GitHub Pages site</a>