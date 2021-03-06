# BLTH  
**Bilibili Live Tasks Helper**  

![TamperMonkey 4.10](https://img.shields.io/badge/TamperMonkey_4.10-pass-green.svg) ![Chromium 83](https://img.shields.io/badge/Chromium_83-pass-green.svg) ![Firefox 77](https://img.shields.io/badge/Firefox_77-pass-green.svg)
+ 在 Tampermonkey 脚本设置中需要将此脚本的设置 “仅在顶层页面（框架）运行” 设置为否(默认为否)才使脚本在特殊直播间运行。  
+ 不保证能通过其它油猴插件(Greasemonkey/Violentmonkey等)运行。  

-------------------------------

### 安装方法
### 1. 点击 [BLTH_raw](https://raw.githubusercontent.com/andywang425/BLTH/master/B%E7%AB%99%E7%9B%B4%E6%92%AD%E9%97%B4%E6%8C%82%E6%9C%BA%E5%8A%A9%E6%89%8B.user.js) 从 githubusercontent 安装脚本    
### 2. 点击 [BLTH_Origin_greasyfork](https://greasyfork.org/zh-CN/scripts/406048-b%E7%AB%99%E7%9B%B4%E6%92%AD%E9%97%B4%E6%8C%82%E6%9C%BA%E5%8A%A9%E6%89%8B) 或 [BLTH_Origin_openuserjs](https://openuserjs.org/scripts/andywang425/B%E7%AB%99%E7%9B%B4%E6%92%AD%E9%97%B4%E6%8C%82%E6%9C%BA%E5%8A%A9%E6%89%8B) 前往 greasyfork/openuserjs 安装脚本  

带有Origin字样的为原格式脚本，其余为压缩脚本。建议安装压缩脚本。  

-------------------------------

### 使用方法 
在Tampermonkey中启用脚本，登陆bilibili后打开任意b站直播间。 

-------------------------------

### 一些建议
+ 初次使用时若出现看不到控制面板的情况，请等待一会或尝试刷新页面。  
+ 部分设置更改后需要刷新页面才能生效。  
+ 使用前建议先关闭广告拦截插件，并确认相关浏览器设置(如cookie权限，脚本拦截)否则该脚本可能无法正常运行。  
+ 修改浏览器Referer设置

   建议通过修改浏览器设置不发送或缩减Referer。
   + Chrome  
   在地址栏输入`chrome://flags/`，搜索`Reduce default 'referer' header granularity`和`Prefetch request properties are updated to be privacy-preserving`，将这两个功能设置为`Enabled`。
   + FireFox  
   在地址栏输入`about:config`，搜索`network.http.sendRefererHeader`，把这个设置的值改为`0`。


交流群:[1106094437](https://jq.qq.com/?_wv=1027&k=fCSfWf1O)（入群问题答案：B站直播间挂机助手），欢迎进来聊天或者提点建议~    

-------------------------------

## 功能细节 

脚本窗口可以上下滚动！部分设置可能需要滚动后才能看到。
点击**直播画面上方**按钮隐藏/显示脚本窗口和提示信息。    

<details>
<summary>自动参加礼物抽奖</summary>
<ul>
<li>抽奖前随机延迟</li>
<li>特定时段不参与抽奖</li>
<li>随机跳过抽奖</li>
<li>可设置当天最多抢辣条数量</li>
<li>抽奖前模拟进入目标房间</li>
<li>抽奖前发送活跃弹幕（防检测）</li>
<li>被风控后强制重复抽奖直到成功，最多尝试5次</li>
</ul>
</details>
<details>
<summary>自动参加实物（金宝箱）抽奖</summary>
<ul>
<li>忽略含特定关键字或匹配特定正则表达式的存疑抽奖</li>
</ul>
</details>
<details>
<summary>自动参与天选时刻</summary>
<ul>
<li>忽略所需金瓜子大于设置值的天选</li>  
<li>含特定关键字或匹配特定正则表达式的存疑天选</li>  
<li>保存当前关注列表为白名单</li>  
<li>取关不在白名单内的UP主</li>   
</ul>
</details>
<details>
<summary>自动完成主站每日任务</summary>
<ul>
<li>登陆主站</li>  
<li>观看视频</li>  
<li>自动投币（可指定给某用户的视频投币）</li>  
<li>分享视频</li>   
</ul>
</details>
<details>
<summary>屏蔽不必要的内容</summary>
<ul>
<li>移除2233模型</li>
<li>移除活动入口</li>
<li>移除排行榜</li>
<li>屏蔽挂机检测</li>
</ul>
</details>
<li>自动获取小心心</li>
<li>自动点亮勋章</li>
<li>自动送礼</li>
<li>银瓜子换硬币</li>
<li>直播区签到</li>
<li>应援团签到</li>
<li>自动参加被广播的节奏风暴</li>
<li>自动发弹幕</li>
<li>快捷购买粉丝勋章</li><br>

-------------------------------

## 说明
#### 关于脚本代码格式
本脚本在三个平台上的代码格式有所不同
+ github: 压缩和原格式都有
+ openuserjs: 第一次安装为原格式，若用tampermonkey更新则会变为压缩格式
+ greasyfork: 原格式

注：项目文件中的[B站直播间挂机助手.user.js](https://github.com/andywang425/BLTH/blob/master/B%E7%AB%99%E7%9B%B4%E6%92%AD%E9%97%B4%E6%8C%82%E6%9C%BA%E5%8A%A9%E6%89%8B.user.js)是压缩后的脚本。  
原格式的脚本为[B站直播间挂机助手.js](https://github.com/andywang425/BLTH/blob/master/B%E7%AB%99%E7%9B%B4%E6%92%AD%E9%97%B4%E6%8C%82%E6%9C%BA%E5%8A%A9%E6%89%8B.js)。  

#### 输入数据格式
+ 浮点数(小数)或整数: 抽奖-抽奖前附加随机延迟，随机跳过礼物；弹幕-发送时间（或时间格式）。  
+ 数组(或单个数据): 送礼-优先送礼房间，不送礼房间；小心心-自动点亮勋章房间号；弹幕-房间号，间隔时间(此项可填浮点数)；抽奖-忽略关键字。  
+ 其余只支持整数。  

#### 自动送礼
+ 若不勾选【无视礼物类型和到期时间限制】，自动送礼只会送出辣条，亿圆和小心心。  
+ 如果要填写多个优先送礼房间或不送礼房间，每个房间号之间需用半角逗号`,`隔开。如 666,777,888 (其实就是数组的格式)。若不勾选送礼优先高等级粉丝牌则优先送低等级粉丝牌。  
+ 礼物到期时间: 将要在这个时间段里过期的礼物会被送出(勾选【无视礼物类型和到期时间限制】时无论是否将要过期都会被送出)。  
+ 送礼设置优先级:  
  不送礼房间 > 优先送礼房间 > 优先高/低等级粉丝牌。  
+ 送礼设置逻辑规则:  
  无论【优先高/低等级粉丝牌】如何设置，会根据【无视礼物类型和到期时间限制】（勾选则无视是否到期补满亲密度，否则只送到期的）条件去按优先送礼房间先后顺序送礼。  
  之后根据【优先高/低等级粉丝牌】决定先送高级还是低级。  
+ 若不勾选【无视礼物类型和到期时间限制】，不会送出永久礼物。  
+ 【剩余礼物】指送满了所有粉丝牌，但仍有剩余的将在1天内过期的礼物。  
+ 【剩余礼物送礼直播间】填0则不送剩余礼物。  

#### 自动投币
+ 脚本会根据今日你已获得的投币经验值判断你已经投了多少个币，然后自动投剩余没投的币。  

  >如今日已获得投币经验20，脚本投币数量设置为4，则会投2个币。  

+ 【给用户(UID:___)的视频投币】若填0则给动态中的视频依次投币(不存在UID为0的用户)。  

#### 任务执行时间
+ 初次启用某一项任务时立刻执行。  
+ 登陆主站，观看视频，自动投币，分享视频，银瓜子换硬币，领银瓜子宝箱，直播区签到每日凌晨0点1分时时执行。  
+ 应援团签到在第二天早上8点执行。  

#### 节奏风暴
+ 仅会参加被广播的节奏风暴。若无法参加请尝试实名后再参加。  
+ 这个功能目前处于实验阶段，且风险较大。  

#### 内容屏蔽
+ 【屏蔽挂机检测】脚本每十分钟触发一次页面可见性改变事件防检测。  

#### 小心心
+ 通过发送客户端心跳包获取小心心（无论目标房间是否开播都能获取）。检测到包裹内有24个7天的小心心后会停止。  
+ 在获取完所有小心心之前直播间不刷新。  
+ 点亮勋章指送出一个小心心；点亮勋章会在自动送礼之前进行，也可以点击按钮立刻执行。  
+ 不会点亮自动送礼中的【不送礼房间】的勋章。  
+ 若不勾选【点亮勋章时忽略亲密度上限】，则仅会点亮当日剩余亲密度大于等于小心心亲密度的勋章。   
+ 勋章点亮模式说明
  + 白名单：点亮【自动点亮勋章房间号】所对应的粉丝勋章。
  + 黑名单：点亮所有粉丝勋章中除了【自动点亮勋章房间号】所对应勋章的粉丝勋章。  
  _提示：如果想点亮所有勋章，选黑名单然后不填写拥有勋章的房间号即可。_  
+ B站随时可以通过APP客户端热更新使该功能失效。  

#### 弹幕设置
+ 弹幕内容，房间号，发送时间可填多个，数据之间用半角逗号`,`隔开(数组格式)。脚本会按顺序将这三个值一一对应，发送弹幕。  
+ 若有多条弹幕需要发送，每条弹幕间会有1.1秒的间隔时间。  
+ 如果数据没对齐，缺失的数据会自动向前对齐。如填写`弹幕内容 lalala`，`房间号 3,4`，`发送时间 5m,10:30`，少填一个弹幕内容。那么在发送第二条弹幕时，第二条弹幕的弹幕内容会自动向前对齐（即第二条弹幕的弹幕内容是lalala）。  
+ 发送时间有两种填写方法

  1.【小时】h【分钟】m【秒】s  
  + 每隔一段时间发送一条弹幕
  + 例子：`1h2m3s`, `300m`, `30s`, `1h50s`, `2m6s`, `0.5h`  
  + 可以填小数
  + 可以只填写其中一项或两项  

  脚本会根据输入数据计算出间隔时间，每隔一个间隔时间就会发送一条弹幕。如果不加单位，如填写`10`则默认单位是分钟（等同于`10m`）。  

  _注意：必须按顺序填小时，分钟，秒，否则会出错(如`3s5h`就是错误的写法)_  

  2.【小时】:【分钟】:【秒】  
  + 在特定时间点发一条弹幕
  + 例子： `10:30:10`, `0:40`  
  + 只能填整数
  + 小时分钟必须填写，秒数可以不填  

  脚本会在该时间点发一条弹幕（如`13:30:10`就是在下午1点30分10秒的时候发弹幕）。  

#### 实物抽奖
+ 【忽略关键字】中每一项之间用半角逗号`,`隔开。  
+ 【忽略关键字】可以填正则表达式。正则格式为以`/`开头且以`/`结尾，如`/测.*试/`。

推荐正则教程：[正则表达式30分钟入门教程](https://deerchao.cn/tutorials/regex/regex.htm) by [deerchao](https://deerchao.cn/)  

+ 【检测到__个不存在活动的aid后停止检测】如果你不理解此项保持默认配置即可。  

#### 天选时刻
+ 【忽略关键字】中每一项之间用半角逗号`,`隔开。  
+ 【忽略关键字】可以填正则表达式。正则格式为以`/`开头且以`/`结尾，如`/测.*试/`。  

分享一个来自群友的正则：`/(([^十百千万拾佰仟01234][零0oO]|^[零0oO])[\.点、。][01234一二三四零壹贰叁肆Oo])|[01234一二三四零壹贰叁肆Oo][分]|(图片|照片|写真|相片|排位|车位|一起|代打|好友|专属头衔|素颜照|卸妆照|美照|皮肤|空气)/`

+ 【请求间隔_毫秒】轮询天选，取关，获取粉丝勋章信息时每两个请求间的间隔时间。如果间隔时间过短可能会被风控。  

  _注：每两个请求间本就存在一个微小的间隔，流程为：发出请求 - 等待回复 - 等待一个间隔时间 - 发出下一个请求。_  
  
+ 【保存当前关注列表为白名单】【取关不在白名单内的UP主】参加天选时会关注很多UP。可以在参加天选前点击【保存当前关注列表为白名单】，参与完天选后再点【取关不在白名单内的UP主】来清理关注列表。不建议频繁清理，可能会被风控。  
+ 轮询的房间来源于各分区小时榜和热门房间列表。  
+ 轮询房间占用资源较多，若出现卡顿请尝试降低【检查房间最大数量】。  

#### 购买粉丝勋章
+ 调用官方api（`api.vc.bilibili.com/link_group/v1/member/buy_medal`），消耗20硬币购买某位UP的粉丝勋章。  
+ 默认值为当前房间号。点击购买按钮后有确认界面，无需担心误触。  

#### 其它设置说明
+ 重置所有为默认：指将设置和任务执行时间缓存重置为默认。  
+ 再次执行所有任务会使相关缓存重置为默认，可以在勾选了新的任务设置后使用。  
+ 支持输入框回车保存。  

#### 运行日志
1. 普通的日志可以点击聊天区上方，大航海右侧的【日志】查看。  
2. 脚本默认开启控制台日志，打开控制台在Filter中输入`IGIFTMSG`即可过滤出本脚本的日志。若想关闭日志可以在脚本头部加入`console.log = () => {}`。  
如果使用脚本过程中遇到问题，可以在控制台中寻找相关错误信息。

#### 关于反馈
反馈bug前请先阅读[bug_report.md](https://github.com/andywang425/BLTH/blob/master/.github/ISSUE_TEMPLATE/bug_report.md)。

-------------------------------

## 已知问题
1. [#12](https://github.com/andywang425/BLTH/issues/12)  
本脚本可能与[Bilibili-Evolved](https://github.com/the1812/Bilibili-Evolved)存在兼容性问题导致脚本窗口无法正确加载。若出现此问题，请尝试在Bilibili-Evolved设置-其它中，将`加载模式`设置为延后，打开`启用Ajax Hook API`。  
2. 脚本每次更新后第一次运行可能会不工作，刷新一下页面即可。   

-------------------------------

## 许可证  
![MIT License](https://img.shields.io/badge/license-MIT-green)  

-------------------------------

## 其它信息  
这个项目的部分代码来源于以下几个项目:  
+ [B站直播心心助手](https://greasyfork.org/zh-CN/scripts/381907-b%E7%AB%99%E7%9B%B4%E6%92%AD%E5%BF%83%E5%BF%83%E5%8A%A9%E6%89%8B) (MIT) by [十六夜](https://greasyfork.org/en/users/289469-%E5%8D%81%E5%85%AD%E5%A4%9C)
+ [BLRHH](https://github.com/SeaLoong/BLRHH) (MIT) by [SeaLoong](https://github.com/SeaLoong)  
+ [Bilibili-LRHH](https://github.com/pjy612/Bilibili-LRHH) (MIT, _forked from SeaLoong/BLRHH_) by [pjy612](https://github.com/pjy612)
+ [TampermonkeyJS](https://github.com/lzghzr/TampermonkeyJS) (MIT) by [lzghzr](https://github.com/lzghzr)  
+ [layer](https://github.com/sentsin/layer) (MIT) by [sentsin](https://github.com/sentsin)  

本脚本使用的库：  
+ [jquery](https://github.com/jquery/jquery) (MIT)  
+ [BilibiliAPI_Mod.min.js](https://github.com/andywang425/BLTH/blob/master/library_files/BilibiliAPI_Mod.js) (MIT)：B站API及常用函数。  
+ [libBilibiliToken.js](https://github.com/lzghzr/TampermonkeyJS/blob/master/libBilibiliToken/libBilibiliToken.js) (MIT)：获取移动端token。  
+ [libWasmHash.js](https://github.com/lzghzr/TampermonkeyJS/blob/master/libWasmHash/libWasmHash.js) (MIT)：WebAssembly实现的Hash，计算心跳请求参数。  
+ [layer.js](https://github.com/sentsin/layer/blob/master/dist/layer.js) (MIT)：创建弹窗，信息框等  

本脚本引用的外部资源：  
+ [layer.css](https://github.com/sentsin/layer/blob/master/dist/theme/default/layer.css)：layer.js的内置样式  

-------------------------------

## 鸣谢
[十六夜](https://greasyfork.org/en/users/289469-%E5%8D%81%E5%85%AD%E5%A4%9C)，[SeaLoong](https://github.com/SeaLoong)，[pjy612](https://github.com/pjy612)，[lzghzr](https://github.com/lzghzr)，[sentsin](https://github.com/sentsin)，[X-Holmes](https://github.com/X-Holmes)  
以及所有提出过建议的用户。

-------------------------------

## 更新日志
>### 5.1
>新功能：实物/天选中奖后通过方糖推送通知；忽略关键字编辑方式优化；新增按钮点击特效；实物/天选参与抽奖后会追踪获奖情况，若中奖则在日志区域显示金色日志，通过方糖推送通知（如果开启），并在日志右上角显示小红点；修复自动投币的一些bug；各种运行效率上的优化。  

完整更新日志见[update-log.md](https://github.com/andywang425/BLTH/blob/master/update-log.md)。  