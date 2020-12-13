# weiyi12
SSM留学中介网站的设计与实现

#### 介绍
本文以实际运用为开发背景，运用软件工程原理和开发方法，使用MYSQL数据库来对信息进行储存，采用JSP技术构建一个JSP留学中介网站的设计与实现。在本JSP留学中介网站的设计与实现的整个开发过程中，首先对系统进行了需求分析，设计出系统的前台和后台功能，用户可进入系统进行留学咨询、关于我们、留学流程、留学新闻、修改用户信息等。系统后台管理员主要实现了系统管理、用户管理、资讯信息管理、资讯分类等。其次对网站进行总体规划和详细设计，总体规划主要包括网站的功能规划，网站总体结构规划，网站的数据结构规划等；详细设计主要包括网站数据库的设计和实现，主要功能模块的具体设计和实现，模块实现的关键代码等。最后对JSP留学中介网站的设计与实现进行了系统测试，并对测试结果进行了分析和总结，进而得出系统的不足及需要改进的地方，为以后的系统维护和扩展提供了方便，同时也为以后开发类似系统提供了借鉴和帮助。
本JSP留学中介网站的设计与实现采用B/S结构，JSP技术、MYSQL数据库进行开发，功能齐全，界面布局合理，操作简单，符合当今社会发展需求。


#### 软件架构
软件架构说明


#### 安装教程

1.  xxxx
2.  xxxx
3.  xxxx

#### 使用说明

1.  xxxx
2.  xxxx
3.  xxxx

#### 参与贡献

1.  Fork 本仓库
2.  新建 Feat_xxx 分支
3.  提交代码
4.  新建 Pull Request

![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/234935_07bd1a37_4865385.png "屏幕截图.png")
JSP留学中介网站的设计与实现需要后台数据库，下面介绍数据库中的各个表的详细信息。

(1)菜单实体数据表如表4-1 sys_menu菜单信息表所示，图中包含菜单及其下属的MENU_ID、MENU_NAME、MENU_URL、MENU_ICON、MENU_TYPE几个数据。
表4-1 sys_menu菜单信息表
序号	列名	数据类型	长度	主键	允许空	说明
1	MENU_ID	Int	11	是	否	编号
2	MENU_NAME	varchar	255	否	是	名称
3	MENU_URL	varchar	255	否	是	网址
4	MENU_ICON	varchar	60	否	是	图标
5	MENU_TYPE	varchar	10	否	是	类型
(2)角色实体数据表如表4-2  sys_role角色信息表所示，图中包含角色以及角色的ROLE_ID、ROLE_NAME、RIGHTS、ROLE_TYPE几个数据。
表4-2  sys_role角色信息表
序号	列名	数据类型	长度	主键	允许空	说明
1	ROLE_ID	Int	100	是	否	编号
2	ROLE_NAME	varchar	100	否	是	名称
3	RIGHTS	varchar	255	否	是	权限
4	ROLE_TYPE	int	2	否	是	角色类型
(3)关于我们实体数据表如表4-3  t_aboutus关于我们信息表所示，关于我们表的内容包含ABOUTUS_ID、TITLE、CONTENT、CREATE_TIME、UPDATE_TIME、CREATE_ID、UPDATE_ID、EMARK、TYPE、IMG_PATH几个数据。
                          表4-3  t_aboutus关于我们信息表
1	ABOUTUS_ID	Int	100	是	否	编号
2	TITLE	varchar	100	否	是	标题
3	CONTENT	varchar	400	否	是	内容
4	EMARK	varchar	400	否	是	备注
5	CREATE_ID	varchar	32	否	是	创建人ID
6	UPDATE_ID	varchar	32	否	是	修改人ID
7	CREATE_TIME	timestamp	100	否	是	创建时间
8	UPDATE_TIME	varchar	100	否	是	修改时间
9	TYPE	int	100	否	是	类型
10	IMG_PATH	varchar	100	否	是	图片地址
(4)资讯类型实体数据表如表4-4 t_msgtype资讯类型信息表所示，资讯类型数据表包含MSGTYPE_ID、MSG_NAME、EMARK、CREATE_ID、UPDATE_ID、CREATE_TIME、UPDATE_TIME几个数据。



表4-4 t_msgtype资讯类型信息表
序号	列名	数据类型	长度	主键	允许空	说明
1	MSGTYPE_ID	varchar	11	是	否	编号
2	MSG_NAME	varchar	100	否	是	标题
3	EMARK	varchar	100	否	是	备注
4	CREATE_ID	varchar	32	否	是	创建人ID
5	UPDATE_ID	varchar	32	否	是	修改人ID
6	CREATE_TIME	varchar	100	否	是	创建时间
7	UPDATE_TIME	varchar	100	否	是	修改时间
(5)新闻实体数据表如表4-5 t_news新闻信息表所示，新闻实体数据表包NEWS_ID、TITLE、CONTENT、EMARK、UPDATE_ID、CREATE_ID、CREATE_TIME、UPDATE_TIME几个数据。
表4-5 t_news新闻信息表
序号	列名	数据类型	长度	主键	允许空	说明
1	NEWS_ID	Int	100	是	否	编号
2	TITLE	varchar	100	否	是	标题
3	CONTENT	varchar	400	否	是	内容
4	EMARK	varchar	400	否	是	备注
5	CREATE_ID	varchar	32	否	是	创建人ID
6	UPDATE_ID	varchar	32	否	是	修改人ID
7	CREATE_TIME	timestamp	100	否	是	创建时间
8	UPDATE_TIME	varchar	100	否	是	修改时间

![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235003_7340f2b0_4865385.png "屏幕截图.png")
管理员需要通过用户名和密码可以进行登录等，其界面如图所示，此界面可以通过输入注册成功之后的用户名以及密码，点击登陆按钮即可登录系统，没有账号的用户可以点击注册按钮跳转至用户注册界面进行注册，点击记住密码系统记住用户密码
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235011_a7bd4377_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235031_8261c415_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235039_1e29f95e_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235046_5173ded0_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235055_d165686d_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235102_0842e81d_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235110_adafb231_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235119_e7d3a74a_4865385.png "屏幕截图.png")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1122/235125_304a5c86_4865385.png "屏幕截图.png")


联系Q：2762501186
![输入图片说明](https://images.gitee.com/uploads/images/2020/1119/003728_cd598bb9_4865385.jpeg "微信.jpg")

#### 特技
