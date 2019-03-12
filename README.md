# RSSHub Docs

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs?ref=badge_shield)
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs.svg?type=small)](https://app.fossa.io/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs?ref=badge_small)

## 为什么

官方文档太卡，打算建立一个项目用来重构

## 内容

只会收录一般大众使用的服务，不常用的服务将不会收录到文档以保证速度和优化。

## 使用

```
git clone https://github.com/JimmyRice/rsshubdocs.git rssdocs

cd rssdocs

sudo npm install -g vuepress
```

### 文档目录：
./docs/content/about:关于页面

./docs/content/install:部署页面

./docs/content/api:指南页面

### VuePress命令

npm run docs:dev 在本地预览，地址:`localhost:8080`

npm run docs:build 生成静态文件到 `./docs/.vuepress/dist/` 文件夹下

## 注意事项
请勿随意更动项目根目录下的`static.json`文件。

请在写入新的内容前先使用`git pull`获取最新版本，修改完后通过`npm run docs:build`生成静态文件后再使用`git push`。

## 其他

### License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2FJimmyRice%2Frsshubdocs?ref=badge_large)

### RSSHub
万物皆可RSS

体验地址:[自建 (花生壳, 可能会宕机, 可用于体验...)](http://jimmy0w0.oicp.io/) / [官方](https://rsshub.app/)
