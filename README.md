# 模块教程
openinstall 模块封装了openinstall平台的SDK，集成了携参安装，渠道统计，快速下载和一键跳转功能；可用于实现移动广告效果统计，免填邀请码，安装后自动加好友，一键加入游戏房间，用户分享统计，微信中快速下载/一键跳转等功能，根据需求可实现更多场景。

**模块地址**：https://www.apicloud.com/mod_detail/openinstall  
**模块示例**：

## 集成使用步骤
1、前往 [openinstall 官网](https://www.openinstall.io/) 注册账号  
2、进入 [openinstall 控制台](https://developer.openinstall.io/)，创建应用。并到“Android集成/iOS集成”菜单获取应用的AppKey、scheme和关联域名(Associated Domains)   
3、到 [openinstall](https://www.apicloud.com/mod_detail/openinstall) 模块详情页中添加模块到应用中  
4、根据 [集成文档](https://docs.apicloud.com/Client-API/Open-SDK/openinstall) 集成 openinstall 模块  
5、集成完成后，通过云编译导出iOS/Android安装包上传 [openinstall控制台](https://developer.openinstall.io/) 对应的应用  
6、通过openinstall的“在线测试”功能进行功能测试验证  
7、功能测试验证通过后，进入[openinstall 控制台](https://developer.openinstall.io/)配置安装包下载地址，根据“web集成”文档开发下载落地页  

## 常见问题  

**问：** 打开网页显示“对应平台的集成工作尚未完成，请登录openinstall查看详情”  
**答：** App端集成完成后，必须上传一次安装包激活后，平台才会正常工作，上传后也更方便集成测试。

**问：** 为什么测试时渠道编号channelCode一直没有返回参数，只有data有参数返回  
**答：** 如果需要测试渠道链接，需要先进入渠道统计模块，创建出渠道链接，扫描对应的渠道链接下载安装测试，才有channelCode返回。

**问：** 每次调用getInstall方法都会回调，会触发业务重复调用  
**答：** SDK内部将会一直保存安装数据，每次调用getinstall方法都会返回值,如果调用了getInstall并处理了自己的业务，后续不想再被触发，那么可以自己在业务调用成功时，设置一个标识，不再调用getInstall方法。

**问：** 应用的下载链接或二维码在哪里获取  
**答：** openinstall平台提供的在线测试二维码、链接和渠道默认二维码、链接都是仅供测试用途的。自己的下载页需要开发者自行开发网页，并且根据“web集成 -> JavaScript集成/banner集成”文档集成openinstall，二维码可以用转换工具将网页链接转换成二维码





