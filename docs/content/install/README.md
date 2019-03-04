---
sidebar: auto
---

# 安装与启动

## 手动部署
安装非常容易，这边介绍npm的食用方式

首先克隆Git仓库并且切换到项目目录下

```
git clone https://github.com/DIYgod/RSSHub.git

cd RSSHub
```

进入之后安装RSSHub所需要的依赖

```
npm install
```

## 常见问题

### 没有权限
将`npm install`改成`sudo npm install`

### 安装过程慢甚至失败

执行：

```
npm install -gd express --registry=http://registry.npm.taobao.org

npm config set registry http://registry.npm.taobao.org
```
然后重新安装

## 启动 <Badge text="默认端口1200" vertical="middle"/>

### 运行
安装完成后，在终端敲下

```
npm start
```

即可启动RSSHub

### 后台运行
如果你需要关闭终端，但是想让它在后台运行，你可以通过nohup来做到

```
nohup npm start &
```

Enjoy it!
