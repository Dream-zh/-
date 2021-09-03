# 实现

 ## 解决目标

实现网页端和移动端的实时交互，用户可以利用配套app对网页进行操控

 ## 命名规范

CSS BEM命名规范 即：

      block 代表了更高级别的抽象或组件
      
      block__element 代表 block 的后代，用于形成一个完整的 block 的整体
      
      block--modifier代表 block 的不同状态或不同版本
      

 ## 开发流程

  ### 页面开发

先通过HTML自带的video组件完成对视频容器的搭建；

使用axios在网页获取后端数据提供给前端显示；

随机生成五位随机数并通过qrcode生成对应二维码，以便后续移动端的绑定匹配；

之后利用将Websocket和轮询机制以及其它的实时通信方式封装成了通用接口的Socket.io来实现双向数据通信，以便后续与手机端交互；

最后css动画animation和ElementUI组件对页面进行美化。

  ### app开发

因为Hbuild X的兼容性优势，采用其开发移动端；

同样利用Socket.io来实现双向数据通信和axios在网页获取后端数据提供给前端显示，用于pc端交互；

使用vue-awesome-mui实现移动端扫描二维码与pc端进行绑定匹配；

最后使用ElementUI组件对页面进行美化。

# 使用

![5KMREN4%OBUWA0O_C4YJ)MC](https://user-images.githubusercontent.com/65300014/131882326-ce62a3c9-1b53-4235-b345-78f493038975.png)

第一次使用该页面时需要前往下载页面下载手机app

![C9CMB4Z 6MYK4}}YT2XKPZ9](https://user-images.githubusercontent.com/65300014/131882609-8f01a916-b73e-4d1c-bd2e-c452a2c7b574.png)

在遥控器的导航栏第二项集选位置，选择需要播放的视频即可


# 设想

直播视频播放页面与登录

实时聊天和弹幕池

手机端交互，提供对应下载（是否额外写页面）

视频登录加密

敏感词汇替换

登陆后手机端二维码登陆（提前？）

评论区，分页单楼回复

性能优化，视频加载


# 总结 

由于直播接口免费次数测试的时候使用完了，我们小组临时决定更改了目标。所以成品可能存在一些缺陷，包括服务器在内视频加载和读取可能会间歇性失效（突然失效过会又好，和网络有关），也请劳烦字节的各位大大测试的时候集选处可以多尝试一下。

大部分设想我们没有完全实现，不过这个项目以后我们还是会持续更新下去。
简单说一下本次项目实践的收获，在开发流程中我们按照目前部分开发采用github的分支操作，感受偏向于工作中开发的具体操作流程是什么。对于前后端的交互，二维码生成，手机app开发流程等开发过程有了新的理解和效果呈现。
