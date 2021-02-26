 [![Python 3.7](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-370/)
 [![itchat_vesion](https://img.shields.io/badge/Itchat-1.3.10-brightgreen.svg)](https://github.com/littlecodersh/ItChat)
 [![EverydayWechat](https://img.shields.io/badge/sfyc23/Powered%20By-EverydayWechat-brightgreen.svg)](https://github.com/sfyc23/EverydayWechat/)
 [![GitHub issues](https://img.shields.io/github/issues/why2lyj/youxiang.svg)](https://github.com/why2lyj/youxiang/issues)
 [![Page Views Count](https://badges.toozhao.com/badges/01EJD3TT6C1J7T283S3A3JZGE3/green.svg)](https://badges.toozhao.com/stats/01EJD3TT6C1J7T283S3A3JZGE3 "Page Views Count")
 

 
## 项目背景

无非就是想撸羊毛，自己又懒的一个一个找，一个一个发。已知目前的返佣app非常的多，比如：好省，蜜源，粉象生活，高佣联盟，芬香，花生日记，惠鲸等等。归根到底无非是利用淘宝、京东、拼多多、苏宁的开放平台做的。所以想到是否可以利用已有的开放平台来做一个属于自己的撸羊毛项目。

其实说白了就是 ：
1. 建立微信群 
2. 向微信群里发送自己的推广链接和商品图片
3. 剩下的尽人事听天命了

## 功能说明

项目主要参考 [EverydayWechat](https://github.com/sfyc23/EverydayWechat)

-  支持对多个微信好友自动回复。  （保留原[EverydayWechat](https://github.com/sfyc23/EverydayWechat)功能，自动回复仅保留**智能闲聊（腾讯）**）
-  群助手功能，仅保留进群自动回复及@时自动回复功能。
-  淘宝优惠券自动分发。 
   > 创建定时任务，通过api获取淘宝推广客的优惠信息，发送到群聊。
-  京东优惠券自动分发。
   > 创建定时任务，通过api获取京东联盟的优惠信息，发送到群聊。
-  拼多多优惠券自动分发。
   > 创建定时任务，通过api获取多多进宝（多宝客）的优惠信息，发送到群聊。
-  苏宁易购优惠券自动分发。
   > 创建定时任务，通过官方sdk获取苏宁联盟（苏宁推客）的优惠信息，发送到群聊。
-  唯品会优惠券自动分发（未完成）。
   > 创建定时任务，通过官方sdk获取唯品会的优惠信息，发送到群聊。
   
## 对于微信Web端无法登陆的小伙伴请注意

由于使用的是Itchat框架，此框架仅支持还能用web版微信的人，如web版本微信已经无法使用，本项目无法继续操作。

如果您需要制作自己的微信机器人，推荐使用`wechaty`，详情请访问：https://wechaty.js.org/ ，这是市面上唯一一家提供终身免费`token`服务的微信机器人供应商。

其公司句子科技对于的贡献者会提供免费的`token`，对于开发级贡献者同时会提供专有服务器；如果懒，付费我也不拦着，付费`token`200/月/号。

本项目已完成`python-wechaty`版本迁移。代码私有，不再公开。

如有需要帮助，请主动扫描本页最后的二维码与作者联系。

## 配置信息

仅介绍**推广客设置**，其余配置请参考[EverydayWechat](https://github.com/sfyc23/EverydayWechat)，不做多余赘述。

参数说明：

淘宝联盟

| 名称 | 示例       | 必填 | 说明 |
| -------- | -------------- | ---------- |---------- |
| is_open | True/False | 必填 | 是否开启淘宝联盟推广|
| app_key | 淘宝联盟 app_key | 必填 | 淘宝联盟申请下来的 app_key |
| app_secret | 淘宝联盟 app_secret | 必填 | 淘宝联盟申请下来的 app_secret |
| adzone_id | 淘宝联盟广告位 | 必填 | 淘宝联盟推广中的广告位 |
| chat_groups |  | 必填 | 详情见举例 |
| group_name | 群名称 | 必填 | 对应微信群的群名称 |
| group_material_id | 物料id | 必填 | 淘宝联盟[material_id](https://market.m.taobao.com/app/qn/toutiao-new/index-pc.html#/detail/10628875?_k=gpov9a)|
| minute | 分钟 | 必填 | 定时任务对应的分钟，逗号分隔，注意空格 |
| hour | 小时 | 必填 | 定时任务对应的小时，逗号分隔，注意空格 |

京东联盟

| 名称 | 示例       | 必填 | 说明 |
| -------- | -------------- | ---------- |---------- |
| is_open | True/False | 必填 | 是否开启京东联盟推广|
| app_key | 京东联盟 app_key | 必填 | 京东联盟申请下来的 app_key |
| app_secret | 京东联盟 app_secret | 必填 | 京东联盟申请下来的 app_secret |
| site_id | 京东联盟网站id或app id | 必填 | 京东联网站id或app id |
| chat_groups |  | 必填 | 详情见举例 |
| group_name | 群名称 | 必填 | 对应微信群的群名称 |
| group_material_id | 物料id | 必填 | 京东联盟物料id|
| minute | 分钟 | 必填 | 定时任务对应的分钟，逗号分隔，注意空格 |
| hour | 小时 | 必填 | 定时任务对应的小时，逗号分隔，注意空格 |

拼多多（多多进宝、多多客）

| 名称 | 示例       | 必填 | 说明 |
| -------- | -------------- | ---------- |---------- |
| is_open | True/False | 必填 | 是否开启拼多多推广|
| app_key | 拼多多 Client_id | 必填 | 拼多多申请下来的 Client_id |
| app_secret | 拼多多 Client_secret | 必填 | 拼多多申请下来的 Client_secret |
| site_id | 推广位 | 必填 | 利用拼多多[接口](https://open.pinduoduo.com/application/document/apiTools?scopeName=pdd.ddk.goods.pid.generate&catId=12)得到的推广位`pid` |
| chat_groups |  | 必填 | 详情见举例 |
| group_name | 群名称 | 必填 | 对应微信群的群名称 |
| group_material_id | 栏目 | 非必填 | 保留字段，底层无用|
| minute | 分钟 | 必填 | 定时任务对应的分钟，逗号分隔，注意空格 |
| hour | 小时 | 必填 | 定时任务对应的小时，逗号分隔，注意空格 |

苏宁易购（苏宁推客）

| 名称 | 示例       | 必填 | 说明 |
| -------- | -------------- | ---------- |---------- |
| is_open | True/False | 必填 | 是否开启苏宁推广|
| app_key | 苏宁易购 appKey | 必填 | 苏宁易购开放平台新建应用的 appKey |
| app_secret | 苏宁易购 secretKey | 必填 | 苏宁易购开放平台新建应用的 secretKey |
| ad_book_id | 推广位 | 必填 | 利用苏宁联盟得到的推广位 |
| chat_groups |  | 必填 | 详情见举例 |
| group_name | 群名称 | 必填 | 对应微信群的群名称 |
| group_material_id | 栏目 | 非必填 | 保留字段，底层无用|
| minute | 分钟 | 必填 | 定时任务对应的分钟，逗号分隔，注意空格 |
| hour | 小时 | 必填 | 定时任务对应的小时，逗号分隔，注意空格 |

**”实例1**，每天7点到23点，每小时的第10分，第40分，将淘宝物料id:19810，发送至群聊 <口碑KFC必胜客麦当劳优惠券>：
> {group_name: '口碑KFC必胜客麦当劳优惠券', group_material_id: '19810', minute: '10,40', hour: '7-23'}

**实例2**，每天7点，12点，15点的第30分，将淘宝物料id:3767,27448,13367,3788的优惠券，发送至群聊 <淘宝内部优惠群-女装类①> ：
> {group_name: '淘宝内部优惠群-女装类①', group_material_id: '3767,27448,13367,3788', minute: '30', hour: '9,12,15'}

*提示* 在运行程序前确保群名已经有且已经保存到通讯录

## 前提准备

---

要使用淘宝联盟的api，需要三个东西：`App Key` ， `App Secret`，广告位`adzone_id`

申请参考：

申请淘宝联盟api：
[申请地址](https://pub.alimama.com/?spm=a219t.7664554.a214tr8.19.2f5835d9zBLGBR)
[文档参考](https://open.taobao.com/doc.htm?docId=73&docType=1)

努力看文档操作，获取到 `App Key` 和 `App Secret`，同时利用商品推广得到 广告位 `adzone_id`

---

要使用京东联盟api，需要`App Key` ， `App Secret`，站点ID`siteId`，还有一个suowo的`token`

申请参考：

申请京东联盟api：
[申请地址](https://union.jd.com/)
[文档参考](https://union.jd.com/helpcenter/13246-13247-46301)

要使用京东联盟获取推广优惠券需要有siteId(站点ID是指在联盟后台的推广管理中的网站Id、APPID)，此申请需要网站备案或有实际app。如没有尽早申请。

另外由于京东联盟生成短址的接口需要申请，申请资质要求（[参考](https://union.jd.com/helpcenter/13246-13247-46301)）目前非力所能及，故采用[suo.mi](https://suowo.cn/)转换短址，区别如下：

| 名称 | 短址示例       | 说明 |
| -------- | -------------- | ---------- |
| 京东短址 | [http://u.jd.com/XXXX](https://github.com/why2lyj/youxiang) | api申请门槛高|
| 缩我短址 | [http://suo.mi/XXXX](https://github.com/why2lyj/youxiang) | 门槛低，免费|

*关于短址：建议选择微信或腾讯的短址服务进行转换以免被屏，没用的另外原因是没有相关token，其他网络上的api没有遇到合适的。*

*缩我短址在2020年7月更变域名suowo.cn，原有suo.mi依然可用，所以作者并无相关代码更变*

---

申请苏宁易购的api请直接参考以下文档，文档来自苏宁联盟的接口人： 

[苏宁联盟开放平台API接入操作指导2.7-20200526.pdf](images/苏宁联盟开放平台API接入操作指导2.7.pdf)

--- 

申请拼多多api接口，需要`Client_id`，`Client_secret`，推广位`pid`

申请拼多多(多多客)api：

首先去拼多多开放平台申请一个应用 [申请地址](https://open.pinduoduo.com/)，得到`Client_id`和`Client_secret`，然后去多多进宝绑定`Client_id`后可以调用接口[接口文档](https://jinbao.pinduoduo.com/third-party/rank)，利用接口得到推广位`pid`

*拼多多接口每天调用仅5000次*

--- 
申请唯品会api：

申请唯品会只能是机构账户，机构账户的申请需要工商营业执照。如果没有营业执照的小伙伴，去[订单侠](https://www.dingdanxia.com/)申请调用api，这个是唯品会官方建议的。

如果你有工商营业执照，请查看文档继续申请[唯品会联盟API接入流程文档v1.9.pdf](images/唯品会联盟API接入流程文档v1.9.pdf)

吐槽下唯品会，申请贼费劲，审核极慢，提交申请近一个月，才有回复。最后是加了一位唯品会内部负责人的微信才问明白。

作者没有工商营业执照，所以...也不打算继续处理唯品会了。

有消息称唯品会将于2021年7月份开放个人开发者api，若开放，本项目会主动添加该功能。尽情知晓。

## 快速启动

直接下载此项目或 clone 项目到本地。  

使用 pip 安装依赖:

```
pip3 install -r requirements.txt
# 或者是使用 pip
# pip install -r requirements.txt
```
运行：
```python
python main.py
```

扫码后，即可使用。

如果你想使用docker启动（请确保`_config.yaml`文件已改成指定）

1. 首先创建镜像，运行
   ```shell
   docker build -f Dockerfile -t youxiang:v1.0.0
   ```
   
2. 启动容器，运行
   ```shell
   docker run -it -d --name youxiang youxiang:1.0.0
   ```
3. 运行以下脚本获取二维码，然后微信登陆
   ```shell
   docker logs -f --tail=1000 youxiang
   ```

如果你不想每次都进容器改`_config.yaml`在第2步的时候可以将项目目录映射到本地
  ```shell
  docker run -it -d -v $pwd:/youxiang --name youxiang youxiang:1.0.0
  ```
## 示例截图：
---
淘宝：

![发送淘宝优惠信息](https://github.com/why2lyj/youxiang/blob/master/images/yangli.jpg?raw=true)

---
京东：

![发送京东优惠信息](https://github.com/why2lyj/youxiang/blob/master/images/jdyangli.jpg?raw=true)

---
拼多多：

![发送拼多多优惠信息](https://github.com/why2lyj/youxiang/blob/master/images/pddyangli.jpg?raw=true)

---
苏宁易购：

![发送苏宁优惠信息](https://github.com/why2lyj/youxiang/blob/master/images/suningyangli.jpg?raw=true)

## 声明

**禁止将本工具用于商业用途**，如产生法律纠纷与本人无关。  

本项目已经完全迁移至非Web端版本（`python-wechaty`版本），后期仅维护bug，不再增添新的功能，还请各位小主知晓。

## Credits 致谢

本项目受以下项目或文章启发，参考了其中一部分思路，向这些开发者表示感谢。  
- [EverydayWechat](https://github.com/sfyc23/EverydayWechat)
- [python 淘宝OPEN API 调用示例](https://www.jianshu.com/p/f9b5e3020789)

## 最后最后最后还是建个群什么的做下交流。留个二维码。

备注写【github】，否则不同过哦。
![加不加随意](https://github.com/why2lyj/youxiang/blob/master/images/6050dfdc-dfef-43c0-94b8-33148f6f5bd8.jpg?raw=true)

## 加个starchart，在此感谢您能够专心致志的读到这里，给项目点个赞吧~
 [![Stargazers over time](https://starchart.cc/why2lyj/youxiang.svg)](https://starchart.cc/why2lyj/youxiang)
