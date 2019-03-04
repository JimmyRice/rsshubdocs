# RSSHub Docs

## 为什么

官方文档太卡，打算建立一个项目用来重构

## 内容

只会收录一般大众使用的服务，不常用的服务将不会收录到文档以保证速度和优化。

## 使用

```
git clone https://github.com/JimmyRice/rsshubdocs.git rssdocs

cd rssdocs

sudo npm install
```

### 文档目录：
./docs/content/about:关于页面

./docs/content/install:部署页面

./docs/content/api:指南页面

## 更新注意事项

请在写入新内容前先使用`git pull`获取最新版本，写入完成后先生成静态文件再通过`git push`提交。

## VuePress命令

npm run docs:dev 在本地预览，地址:`localhost:8080`

npm run docs:build 生成静态文件到 `./docs/.vuepress/dist/` 文件夹下

## Powered By
Powered By Heroku & RSSHub

## 注意事项
请勿随意更动项目根目录下的`static.json`文件。
