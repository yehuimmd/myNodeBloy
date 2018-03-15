# myNodeBloy
Nodejs+MongoDB+jQuery+Bootstrap-esj搭建的个人简易博客

### 主要功能
- 前台 ：进入首页
  
  - 文章查看及文章分类：可自行在项目中增加自己喜欢的文章类型。
  - 留言板
  
 - 后台
 
   - 管理员登录
   - 注册（这两部分用到了node的加密处理）
   - 写博客（word）
   - 管理博客（增删改查）
   - 查看访问用户的位置信息
   
### 项目目录

    db  数据库文件夹
    model 模块目录
    ---- db.js      封装了对数据库的操作（增删改查）
    ---- md5.js     封装了md5加密函数
    ---- setting.js 封装了对数据库的接口
    node_modules 项目依赖包
    public 静态资源目录
    routers 路由目录
    ---- router.js  对请求接口的统一处理
    views 模板目录
    app.js 入口文件
    package.json 文件依赖配置包
  
### 模块分析
 - app.js入口文件
 
   - 引用node的express库——调用
   - 请求设置：就是前端各事件的请求接口设置
   - 监听端口号
   
 - db.js
 进行连接数据库操作，及多数据库进行增删改查等操纵，即文章数据条实现分页。
 
 - router.js
 得到前端的请求，对请求做出响应，也就是对请求接口功能的实现。
 
 - view
 
 渲染前端模块：前端页面的请求数据，部分是通过ejs直接渲染，部分是通过ajax拉取，然后渲染到页面上。

### 注意
- 环境自行安装node及MongoDB，和MongoDB可视化工具roboMongoDB
- 开启数据库：  mongod --dbpath url（项目目录中MongoDB存放的路径，相对路径）整个命令是在你的电脑中安装的MongoDB数据库的bin目录下执行。

### 总结
 自己对搭博客的大致框架也能理清，前期自己也用node搭建过简单的博客网站，
 但是对node包目录的概念还没有掌握清楚，但是通过对该项目的练习，自己也加深了对你的node包目录及模块的理解。
