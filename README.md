# WeChatMoments
微信朋友圈Demo

实现流程
1.需求分析
  本功能旨在做一个微信朋友圈小Demo需求如下:
   ①View包含个人资料图片,头像,推文
   ②对已每一条推文,都会有一个发件人,可选内容,可选图片和评论,除了不包含这个的
   ③一个推文包含0-9张图像,确保视图像微信一样
   ④首先将所有的推文加载到内存中,然后每次异步从内存中获取5条;
   ⑤上拉刷新五条推文
   ⑥下拉刷新显示所有推文的前五条
   ⑦界面要适配各个Android设备
2.详细设计
  界面设计
  ①使用recyclerView实现推文列表,设计adapter,和不同类型的list_item,使用
  ②使用三级缓存模式自定义图片加载框架
  数据库设计
  存储推文,无网络状态下显示存储的推文
  网络数据
  使用okhttp从网络获取数据,使用Gosn解析数据,
3.编码步骤:
  ①引入要使用的第三方library  DiskLruCache,Gson
  ②自定义实现图片加载框架
  ③实现从接口获取和解析数据
  ④将数据持久化(可选)
  ⑤画出UI界面实现上拉加载和下拉刷新
  ⑥数据对接
4.测试.
  
