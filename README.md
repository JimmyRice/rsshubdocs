# RSSHub Docs

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs?ref=badge_shield)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs.svg?type=small)](https://app.fossa.io/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs?ref=badge_small)
[![Netlify Status](https://api.netlify.com/api/v1/badges/c2a54160-6a7b-4007-b8e4-3442136c3a26/deploy-status)](https://app.netlify.com/sites/amazing-murdock-a9cad8/deploys)

`2019/3/28`全面替换成yarn

`2019/4/16`加入Travis CI，免去手动Build

## 为什么

官方文档太卡，打算建立一个项目用来重构

## 内容

只会收录一般大众使用的服务，不常用的服务将不会收录到文档以保证速度和优化。

## 使用

```
git clone https://github.com/JimmyRice/rsshubdocs.git rssdocs

cd rssdocs

sudo yarn install
```

### 文档目录：
./docs/content/about:关于页面

./docs/content/install:部署页面

./docs/content/api:指南页面

### VuePress命令

sudo yarn docs:dev 在本地预览，地址:`localhost:8080`

## 注意事项
请勿随意更动项目根目录下的`static.json`和`.travis.yml`文件。

## 其他

### License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs?ref=badge_large)

### RSSHub
万物皆可RSS

体验地址:[官方](https://rsshub.app/)

## 感谢

Powered By RSSHub / Heroku / VuePress
