# Homework-Assistant
学委作业助手，你的学习好帮手

### 学委作业助手小程序码（长按扫描小程序码查看示例）
<center>
 <img src="/images/xwzs.jpg" margin=20% width=30% />
</center>

### 主要功能页面展示

<div style="display:flex;justify-content:space-around;"> 
 <img src="/images/bg.png" margin=20% width=30% />
 <img src="/images/myclass.png" margin=20% width=30% />
 <img src="/images/myhomework.jpg" margin=20% width=30% />
</div>

<div style="display:flex;justify-content:space-around;"> 
 <img src="/images/workdetails.jpg" margin=20% width=30% />
 <img src="/images/announce.png" margin=20% width=30% />
 <img src="/images/add.png" margin=20% width=30% />
</div>

<br>

<div style="display:flex;justify-content:space-around;"> 
 <img src="/images/set.png" margin=20% width=30% />
 <img src="/images/setmanager.jpg" margin=20% width=30% />
 <img src="/images/managerclass.jpg" margin=20% width=30% />
</div>

#### 2018年8月23日 星期四

1.设计项目的UI布局<br>
2.基本完成项目的UI<br>
3.完善了分享以后的跳转以及传值逻辑<br>
4.完善各表单页面的post逻辑<br>

#### 2018年8月24日 星期五

1.UI界面完成，逻辑部分还未与服务端结合<br>

**近期感悟：感觉不能同一时间同时搞好几个项目，会容易感到迷茫和困惑，进而感到烦躁，降低coding效率。分清事情的轻重缓急以及重要程度，再去动手。所以学委助手这边我准备先放一放，但是会在开学第一周前做完上线！！**


#### 2018年9月22日 星期六 V1

1.因为比较忙，进度好像有、慢，现在正式版本终于上线了哈哈，希望能真正的帮到学委们<br>

#### 2018年9月26日 星期三 V1.1

1.增加了删除已发布作业的功能<br>

#### 2018年10月2日 星期二 V1.2

1.增加 删除创建的班级，退出加入的班级 的功能<br>
2.一些界面按钮的调整<br>
3.增加了作业、公告复制按钮<br>
4.增加了公告的删除功能，修复了“修改公告时候显示的不是当前公告，而是第一次发的公告”的bug<br>

#### 2018年10月5日 星期五 V1.3

1.增加了班级管理员的模块，管理员可以进行除了删除班级和授权管理员之外的其他功能。<br>
2.将updateUser的接口放到了index.js，之前放在app.js会保存不到用户的数据<br>

#### 2018年10月9日 星期二 V1.35

1.修复了用户点击微信群链接进去班级时，没有授权微信名和头像的问题，导致学委在查看管理员时出现null的情况。<br>
2.修复了iphone 7 plus设备上的一些显示错位的bug（myfile部分的微信名 && myclass中删除创建的班级时的弹出框）<br>
3.将workdetails中的内容和备注部分由 ```<view> </view>``` 改为 ```<text> </text>``` 这样子的话，用户在输入时的换行会被保留，更美观<br>

#### 2018年10月12日 星期五 V1.4

1.发布、删除、修改作业和公告或者退出、删除班级的时候不会都统一跳转到主页，而是会相应的在本页面重新加载新数据或者返回上一级页面。<br>
2.增加了功能介绍的部分，也就是在用户第一次创建班级，并进入该班级时，会有一个对功能按钮的高亮介绍。【通过本地缓存实现，如果第一次创建班级并进入时就会设置一个flag为false，此后为true的话就都不会再显示】)<br>

#### 2018年10月15日 星期一 V1.45

1.增加了设置的按钮，放在界面的右侧下方，点击设置按钮，可以选择是否隐藏已结束的作业以及引导用户关注服务号，一边获得新作业提醒。<br>
2.增加了“几天后”、“星期几”的时间标签🏷️，提升用户使用体验。<br>

#### 2018年10月30日 星期二 V1.5
1.增加了修改班级名称的功能，并对界面有一定的改动。<br>
2.设置管理员的界面为开启了服务号消息提醒的用户增加了一个标识。<br>

#### 2018年11月6日 星期二 V1.6
1.增加了文件上传、在线浏览、文件下载的功能。微信在这一块提供的api非常少，所以不得不另辟蹊径，绕了一下实现文件相关的功能<br>
  * 微信并没有提供文件上传的api接口，故在移动端使用webview跳进一个网页中，通过网页中文件上传组件选择并上传文件。同时我们也提供了电脑端上传文件，其实就是将带参的文件上传网址的url给用户复制好，用户粘贴至浏览器访问后，即可上传文件。<br>
  * 在线浏览是通过微信的```wx.downloadFile```来下载文件并用```wx.openDocument```进行浏览。<br>
  * 文件下载的话是将文件的url复制给用户，用户在手机端或者电脑端访问该链接即可下载。<br>
  
2.增加了‘使用指南’，其实就是一个webview指向我们的第一篇介绍推送<br>
3.在班级界面还多了一个班级文件的tabbar，主要是遍历作业数组，然后就每个作业的文件列表concat起来，然后展示<br>

#### 2018年11月14日 星期二 V1.65

1.新增了班级文件直接上传和删除的入口<br>
2.增加了“关于我们”的板块，分为【关于我们】，【更新日志】，【常见问题】三个顶部tabbar<br>
3.修复了修改作业时如果所改的作业无文件时会产生null的bug<br>

#### 2018年11月18日 星期天 V1.7

1.新增了班级分享海报的绘制功能，扫描海报中的小程序码可以快速加入班级，和点击微信群中的小程序链接是相同的功能。<br>
2.修复了修改作业中删除作业配图时会无效的问题。<br>

#### 分享海报图片（扫描带参小程序码可以快速加入班级）
<center>
 <img src="/images/share.jpg" margin=20% width=30% />
</center>

#### 2018年12月9日 星期天 V1.75

1.增加了网络状况不好时的提示。<br>
2.增加了图片转文字的功能，学委可以在发布作业的时候使用。同时也作为一个小实用工具，可以在“我的”页面使用。<br>
3.修复了发布作业时，偶尔会发生图片上传失败的bug。<br>

<div style="display:flex;justify-content:space-around;"> 
 <img src="/images/pictotext.jpg" margin=20% width=30% />
 <img src="/images/origin.jpg" margin=20% width=30% />
 <img src="/images/result.jpg" margin=20% width=30% />
</div>

#### 2018年12月20日 星期四 V1.8

1.增加了"添加到我的小程序"的引导。<br>
2.增加了"开启作业提醒"的公众号引导。<br>
3.增加了语音输入文字的功能，学委发布作业可以更方便<br>
4.增加了催收作业的提醒功能，学委消息提醒能力再升级，并且支持自定义催收作业模板。<br>
5.作业提醒时间由提前两天提醒一次，改成提前三天、提前一天各提醒一次。<br>
6.增加了更新功能的介绍以及“我要反馈”页面中的公众号关注引导。<br>

<div style="display:flex;justify-content:space-around;"> 
 <img src="/images/urge.jpg" margin=20% width=30% />
 <img src="/images/voice.jpg" margin=20% width=30% />
</div>
