<img src="https://avatars.githubusercontent.com/u/56885001?s=200&v=4" alt="logo" width="130" height="130" align="right"/>

[![](https://img.shields.io/badge/TgChat-@UnOfficialV2board讨论-blue.svg)](https://t.me/unofficialV2board)

## 本分支支持的后端
 
 - [修改版XrayR](https://github.com/wyx2685/XrayR)
 - [修改版V2bX](https://github.com/wyx2685/V2bX)
 - [V2bX](https://github.com/InazumaV/V2bX)

## 原版迁移步骤

按以下步骤进行面板文件迁移：

    git remote set-url origin https://github.com/wyx2685/v2board  
    git checkout master  
    ./update.sh  


按以下步骤刷新设置缓存，重启队列:

    php artisan config:clear
    php artisan config:cache
    php artisan horizon:terminate

最后进入后台重新保存主题： 主题配置-主题设置-确定

## 使用 Docker Compose 部署

    git clone --depth 1 https://github.com/UGYnpU2nuB8QCFqDrsWZgmxMBp43WQ/v2board
    cd v2board
    docker compose pull
    docker compose run -it --rm v2board sh init.sh
    docker compose up -d

切记及时记录 密码 和 后台路径

网站默认端口 7002

mysql/mariadb需自行安装

## 使用 Docker Compose 更新 v2board

    cd v2board
    ./update.sh
    docker compose pull
    docker compose down
    docker compose run -it --rm v2board php artisan v2board:update
    docker compose up -d

# **V2Board**

- PHP7.3+
- Composer
- MySQL5.5+
- Redis
- Laravel

## Demo
[Demo](https://demo.v2board.com)

## Document
[Click](https://v2board.com)

## Sponsors
Thanks to the open source project license provided by [Jetbrains](https://www.jetbrains.com/)

## Community
🔔Telegram Channel: [@v2board](https://t.me/v2board)  

## How to Feedback
Follow the template in the issue to submit your question correctly, and we will have someone follow up with you.
