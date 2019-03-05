---
sidebar: auto
---

# 使用指南

## 参数

:::tip ?号和&号
路由地址后面通过`?`号填写参数，通过`&`号可以连接多个通用参数一起组合使用
:::

### 内容过滤

filter可以选出想要的内容

通过:
* filter: 来过滤出标题和描述
* filter_title: 来过滤标题
* filter_description: 来过滤描述
* filter_author: 来过滤作者

用法:
在路由后用`?`开始写入`filter`规则

`filter`后面加上`=`号开始输入过滤内容

也可以通过`|`符号添加多个过滤内容

举例:[https://1931709c.ngrok.io/bilibili/user/video/332704117?filter=%E5%90%84%E7%A7%8D%E5%8F%AF%E7%88%B1](https://1931709c.ngrok.io/bilibili/user/video/332704117?filter=%E5%90%84%E7%A7%8D%E5%8F%AF%E7%88%B1)

filterout可以过滤掉不想要的内容

通过:
* filterout: 来过滤掉不想要的标题和描述
* filterout_title: 来过滤掉不想要的标题
* filterout_description: 来过滤掉不想要的描述
* filterout_author: 来过滤掉不想看到的作者

用法:
和上面一样用`?`和`=`开始写入规则，将filter替换成filterout即可，与上面用法相同；也支持通过`|`建立多个过滤内容

举例:[https://1931709c.ngrok.io/bilibili/user/video/332704117?filterout=%E5%90%84%E7%A7%8D%E5%8F%AF%E7%88%B1](https://1931709c.ngrok.io/bilibili/user/video/332704117?filterout=%E5%90%84%E7%A7%8D%E5%8F%AF%E7%88%B1)

### 条数限制
通过`limit`参数限制最大条数，非常好理解

例如`limit=3`只会抓取最近三条最新的RSS项目

举例:[https://1931709c.ngrok.io/bilibili/user/video/332704117?limit=3](https://1931709c.ngrok.io/bilibili/user/video/332704117?limit=3)

### 自定输出格式
支持RSS2.0与ATOM输出格式

* 缺省RSS2.0: 路由地址，例如[https://1931709c.ngrok.io/bilibili/user/video/332704117](https://1931709c.ngrok.io/bilibili/user/video/332704117)

* RSS 2.0: 路由地址.rss，例如[https://1931709c.ngrok.io/bilibili/user/video/332704117.rss](https://1931709c.ngrok.io/bilibili/user/video/332704117.rss)

* Atom: 路由地址.atom，例如[https://1931709c.ngrok.io/bilibili/user/video/332704117.atom](https://1931709c.ngrok.io/bilibili/user/video/332704117.atom)

:::tip 依然可以使用过滤和条数限制
无论是 `.rss` 还是 `.atom` 在后面加入 `?` 并带有参数都可以使用
:::

## 订阅源 <Badge text="完整版请前往官方文档" vertical="middle" />

### 哔哩哔哩

#### 番剧更新

路由:`/bilibili/bangumi/media/:mediaid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|mediaid|是|番剧ID|

#### UP主投稿

路由:`/bilibili/user/video/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### UP主专栏

路由:`/bilibili/user/article/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### UP主动态

路由:`/bilibili/user/dynamic/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### UP主频道

路由:`/bilibili/user/channel/:uid/:cid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|
|cid|是|频道ID|

#### UP主收藏夹 (主收藏夹)

路由:`/bilibili/user/fav/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### UP主收藏夹 (非主收藏夹，可被自定义追踪)

路由:`/bilibili/fav/:uid/:fid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|
|fid|是|收藏夹ID|

#### UP主投币视频

路由:`/bilibili/user/coin/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### UP主的粉丝

路由:`/bilibili/user/followers/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### UP主的关注

路由:`/bilibili/user/followings/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### 哔哩哔哩分区

路由:`/bilibili/partion/:tid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|tid|是|分区ID|

* 动画分区:

| 分区 | ID |
|------|------|
|MAD.AMV|24|
|MMD.3D|25|
|短片.手书|47|
|综合|27|

* 番剧分区:

| 分区 | ID |
|------|------|
|连载动画|33|
|完结动画|32|
|资讯|51|
|官方延伸|152|

* 国创区:

| 分区 | ID |
|------|------|
|国产动画|153|
|国产原创相关|168|
|布袋戏|169|
|资讯|170|

* 音乐区:

| 分区 | ID |
|------|------|
|原创音乐|28|
|翻唱|31|
|VOCALOID.UTAU|30|
|演奏|59|
|三次元音乐|29|
|OP/ED/OST|54|
|音乐选集|130|

* 舞蹈:

| 分区 | ID |
|------|------|
|宅舞|20|
|三次元舞蹈|154|
|舞蹈教程|156|

* 游戏:

| 分区 | ID |
|------|------|
|单机游戏|17|
|电子竞技|171|
|手机游戏|172|
|网络游戏|65|
|桌游棋牌|173|
|GMV|121|
|音游|136|
|Mugen|19|

* 科技:

| 分区 | ID |
|------|------|
|趣味科普人文|124|
|野生技术协会|122|
|演讲.公开课|39|
|星海|96|
|数码|95|
|机械|98|
|汽车|176|

* 生活:

| 分区 | ID |
|------|------|
|搞笑|138|
|日常|21|
|美食圈|76|
|动物圈|75|
|手工|161|
|绘画|162|
|ASMR|175|
|运动|163|
|其他|174|

* 鬼畜:

| 分区 | ID |
|------|------|
|鬼畜调教|22|
|音MAD|26|
|人力 VOCALOID|126|
|教程|127|

* 时尚:

| 分区 | ID |
|------|------|
|美妆|157|
|服饰|158|
|健身|164|
|资讯|159|

* 广告:

| 分区 | ID |
|------|------|
|广告|166|

* 娱乐:

| 分区 | ID |
|------|------|
|综艺|71|
|明星|137|
|Korea相关|131|

* 影视:

| 分区 | ID |
|------|------|
|影视杂谈|182|
|影视剪辑|183|
|短片|85|
|预告.资讯|184|
|特摄|86|

* 纪录片:

| 分区 | ID |
|------|------|
|全部|177|
|人文.历史|37|
|科学.探索.自然|178|
|军事|179|
|社会.美食.旅行|180|

* 电影:

| 分区 | ID |
|------|------|
|全部|23|
|华语电影|147|
|欧美电影|145|
|日本电影|146|
|其他国家|83|

* 电视剧:

| 分区 | ID |
|------|------|
|全部|11|
|国产剧|185|
|海外剧|187|

#### 分区视频排行榜

路由:`/bilibili/partion/ranking/:tid/:days`

| 参数 | 必要性 | 描述 | 可选值 |
|------|------|------|------|
|tid|是|分区ID|已被规定|
|days|否，可选的|x天内的热度|1-93天|

#### 视频选集列表

路由:`/bilibili/video/page/:aid`

| 参数 | 必要性 | 描述 | 注意 |
|------|------|------|------|
|aid|是|视频ID|AID即AV号，但是请注意视频必须要有选集才可以用该功能|

#### 视频评论

路由:`/bilibili/video/reply/:aid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|aid|是|视频ID|

#### 视频弹幕

路由:`/bilibili/video/danmaku/:aid/:pid`

| 参数 | 必要性 | 描述 |
|------|------|------|       
|aid|是|视频ID|
|pid|否，可选的|分P ID|

#### Link公告

路由:`/bilibili/link/news/:product`

| 参数 | 必要性 | 描述 | 分类 |
|------|------|------|------|
|product|是|公告分类|直播:live, 小视频:vc, 相簿:wh|

### 哔哩哔哩直播

#### 直播开播

路由:`/bilibili/live/room/:roomID`

| 参数 | 必要性 | 描述 |
|------|------|------|
|roomID|是|直播间ID|

#### 直播搜索

路由:`/bilibili/live/search/:key/:order`

| 参数 | 必要性 | 描述 | 分类 |
|------|------|------|------|
|key|是|搜索关键字|无|
|order|是|排序方式|live_time 按照开播时间排序, online 按照人气排序|

#### 直播分区

路由:`/bilibili/live/area/:areaID/:order`

| 参数 | 必要性 | 描述 | 注意 | 分类 |
|------|------|------|------|------|
|areaID|是|分区ID|该ID经常改动，请前往下面给出的链接进行查询|无|
|order|是|排序方式|无|live_time 按照开播时间排序, online 按照人气排序|

[直播分区ID获取](https://api.live.bilibili.com/room/v1/Area/getList)

### 新浪微博
:::warning 注意
获取新浪微博的用户ID请通过在浏览器的Console中输入`$CONFIG.oid`获取
:::

#### 新浪博主 (方案1)

路由:`/weibo/user/:uid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### 新浪博主 (方案2)

路由:'/weibo/user2/:uid'

| 参数 | 必要性 | 描述 |
|------|------|------|
|uid|是|用户ID|

#### 关键词

路由:`/weibo/keyword/:keyword`

| 参数 | 必要性 | 描述 |
|------|------|------|
|keyword|是|搜索关键词

#### 热搜榜

路由:`/weibo/search/hot`

### 贴吧

#### 帖子列表

路由:`/tieba/forum/:kw`

| 参数 | 必要性 | 描述 |
|------|------|------|
|kw|是|贴吧吧名|

#### 精品帖子

路由:`/tieba/forum/good/:kw/:cid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|kw|是|贴吧吧名|
|cid|否，可选的|精品分类|

#### 帖子动态

路由:`/tieba/post/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|帖子ID|

#### 楼主动态

路由:`/tieba/post/lz/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|帖子ID|

### 即刻

#### 主题-精选

路由 (一般情况下):`/jike/topic/:id`

路由 (包含文字):`/jike/topic/text/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|主题ID|

#### 主题-广场

路由:`/jike/topic/square/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|主题ID|

#### 主题-纯文字

路由:`/jike/topic/text/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|主题ID|

#### 用户动态

路由:`/jike/user/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|用户ID|

#### 即刻小报

路由:`/jike/daily`

### 简书

#### 首页

路由:`/jianshu/home`

#### 热门

路由:`/jianshu/trending/:timeframe`

| 参数 | 必要性 | 描述 | 分类 |
|------|------|------|------|
|timeframe|是|设定`周`或`月`时间热门|weekly 按周热门, monthly 按月热门|

#### 专题

路由:`/jianshu/collection/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|专题ID|

#### 作者

路由:`/jianshu/user/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|作者ID|

### 知乎

#### 收藏夹

路由:`/zhihu/collection/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|收藏夹ID|

#### 用户动态

路由:`/zhihu/people/activities/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|用户ID|

#### 用户回答

路由:`/zhihu/people/answers/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|用户ID|

#### 专栏

路由:`/zhihu/zhuanlan/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|专栏ID|

#### 知乎日报

路由:`/zhihu/daily`

#### 知乎热榜

路由:`/zhihu/hotlist`

#### 知乎想法热榜

路由:`/zhihu/pin/hotlist`

#### 问题

路由:`/zhihu/question/:questionId`

| 参数 | 必要性 | 描述 |
|------|------|------|
|questionId|是|问题ID|

#### 话题

路由:`/zhihu/topic/:topicId`

| 参数 | 必要性 | 描述 |
|------|------|------|
|topicId|是|话题ID|

#### 用户想法

路由:`/zhihu/people/pins/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|用户ID|

#### 知乎书店-新书

路由:`/zhihu/bookstore/newest`

#### 知乎想法-24小时新闻汇总

路由:`/zhihu/pin/daily`

### 豆瓣

#### 正在上映的电影

路由:`/douban/movie/playing`

#### 正在上映的高分电影

路由:`/douban/movie/playing/:score/:city`

| 参数 | 必要性 | 描述 |
|------|------|------|
|score|是|大于x分的电影|
|city|否，可选的|城市中文名，默认北京|

#### 即将上映的电影

路由:`/douban/movie/later`

#### 北美票房榜

路由:`/douban/movie/ustop`

#### 豆瓣小组

路由:`/douban/group/:groupid`

| 参数 | 必要性 | 描述 |
|------|------|------|
|groupid|是|豆瓣小组ID|

#### 浏览发现

路由:`/douban/explore`

#### 浏览发现分栏目

路由:`/douban/explore_column/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|分栏目ID|

#### 新书速递

路由:`douban/book/latest`

#### 最新增加的音乐

路由:`/douban/music/latest/:area`

| 参数 | 必要性 | 描述 | 分类 |
|------|------|------|------|
|area|否，可选的|区域类型|chinese 华语区, western 欧美区, japankorean 日韩区|

#### 热门同城活动

路由:`/douban/event/hot/:locationId`

| 参数 | 必要性 | 描述 | 获取方式 |
|------|------|------|------|
|locationId|是|位置ID|通过浏览器Console输入 `window.__loc_id__` 获取|

#### 商务印书馆新书速递

路由:`/douban/commercialpress/latest`

#### 豆瓣书店

路由:`/douban/bookstore`

#### 热门图书排行

路由:`/douban/book/rank/:type`

| 参数 | 必要性 | 描述 | 分类 |
|------|------|------|------|
|type|是|图书类型|fiction 虚构, nonfiction 非虚构|

#### 豆列

路由:`douban/doulist/:id`

| 参数 | 必要性 | 描述 |
|------|------|------|
|id|是|豆列ID|

#### 用户广播

路由:`douban/people/:userid/status`

| 参数 | 必要性 | 描述 |
|------|------|------|
|userid|是|整数型用户ID|

:::warning 提示
目前只支持整数型 id, 字母型的 id，可以通过头像图片链接来找到其整数型 id.

例如用户ID为: `MovieL` 他的头像链接为: `https://img1.doubanio.com/icon/ul1128221-98.jpg`

他的整数ID为: `1128221`
:::

## 更新列表
:::danger 持续更新开启

文档较长，目前已预定更新：

Instagram

抖音

掘金

V2EX

斗鱼直播

AcFun

起点中文网

如果有其他想要添加进来的网站可以通过Issue提出


更详细的文档内容请前往官方文档
:::
