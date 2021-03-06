# 简单记录过程

## windows安装mysql

* [mysql官网](https://www.mysql.com/)
* 进入tab页，downloads，选择MySQL Community (GPL) Downloads
* 选择MySQL Installer for Windows
* 选择大的那个离线安装包，小的那个web版是在线的，一边安装一边下载
* 选择No thanks, just start my download. 
* 可以复制链接到迅雷下载，这样下起来就特别快
* 下好后双击打开，开始安装
* 可以使用默认的，也可以只安装Server Only
* 下一步后选中MySql Server，点击Execute
* 安装之后就可以默认无脑点下一步了，直到Authentication Method选择非默认的Use Legacy Authentication Method
* 设置密码，需要记住密码
* 无脑下一步执行，最后完成
* 桌面此电脑右击管理，选择服务和应用程序，再选择服务，可以找到我们的Mysql80启用或者停用

## windows安装Navicat

* [安装Navicat](https://juejin.im/post/5bc89b3d6fb9a05cea7fbff0)，亲测能激活

## postman文档

* [官方文档](https://learning.postman.com/)

## AJV

* [AJV](https://ajv.js.org/)

## 断言库

* [断言库](https://www.chaijs.com/api/)

## 数据库相关脚本指令

* 先进入后端项目backend
* 在configs新建database.json
```
{
  "development": {
    "host": "127.0.0.1",
    "dialect": "mysql",
    "username": "root",
    "password": "",
    "database": "trello_app_development",
    "timezone": "+08:00"
  },
  "test": {
    "host": "127.0.0.1",
    "dialect": "mysql",
    "username": "root",
    "password": "",
    "database": "trello_app_test",
    "timezone": "+08:00"
  },
  "production": {
    "host": "127.0.0.1",
    "dialect": "mysql",
    "username": "root",
    "password": "",
    "database": "trello_app_production",
    "timezone": "+08:00"
  }
}
```
* 创建数据库和删除数据库指令可以看我的package.json
* 迁移脚本执行`.\node_modules\.bin\sequelize migration:create --name UserInit`
* 更新迁移脚本可以执行`.\node_modules\.bin\sequelize migration:create --name UserAndUpdatedAt`，在使用相关API比如addColumn添加列
* 种子脚本的指令为`.\node_modules\.bin\sequelize seed:create --name UserInit`

