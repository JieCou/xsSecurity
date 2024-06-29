# 介绍
一款多角色在线培训考试系统，系统集成了用户管理、角色管理、部门管理、题库管理、试题管理、试题导入导出、考试管理、在线考试、错题训练等功能，考试流程完善。

# 技术栈
SpringBoot / Shiro / Vue / MySQL

# 产品功能

## 系统完善：完善的权限控制和用户系统
权限控制：基于Shiro和JWT开发的权限控制功能。    
用户系统：用户管理、部门管理、角色管理等。    

## 多角色：多角色支持    
考试端：学生学员角色、支持在线考试、查看分数、训练错题。    
管理端：题库管理、试题管理、考试管理、用户部门管理、查看考试情况等等。    

## 定员考试：考试权限定义    
完全公开：任何人员都可以参与考试。    
指定部门：只有选中部门的人员才可以看到考试。    

## 多题型：常用题型支持    
支持题型：单选题、多选题、判断题。    
难易程度：普通、困难。    

## 便捷组卷：题库组卷    
题库组卷：指定题库、分数、数量；题目、选项随机排序、杜绝作弊    


# 环境要求
JDK 1.8+  [点此下载](https://cdn.yfhl.net/java-win/jdk-8u181-windows-x64.exe)        
Mysql5.7+  [点此下载](https://cdn.yfhl.net/java-win/mysql-installer-community-5.7.31.0.msi)    

# 安装资源

#### 后端

1、安装JDK1.8    
https://cdn.yfhl.net/java-win/jdk-8u181-windows-x64.exe     

2、安装MySQL    
https://cdn.yfhl.net/java-win/mysql-installer-community-5.7.31.0.msi    
-- 安装过程可能需要VC++    
-- https://www.microsoft.com/zh-CN/download/details.aspx?id=40784    
-- 安装数据库管理工具    
https://cdn.yfhl.net/java-win/SQLyog.12.3.1.0.zip    

3、安装IntelliJ IEDA

#### 前端

1、下载安装mvn（nodejs管理器）

2、通过nvm下载安装nodejs（16.x.x及以上版本）

3、安装VS code

# 快速运行  

#### 后端运行

1、自行安装MySQL数据库（版本最好是5.7），将`数据库初始化.sql`导入到安装好的数据库  
2、安装Java环境，要求JDK版本大于1.8  

3、确保maven和java配置好

4、请修改外置配置文件：application-local.yml 改成您自己的MySQL配置  

5、终端运行：mvn spring-boot:run

6、如果无意外，可通过：http://localhost:8101 访问到项目了  
7、管理员账号密码：admin/admin 学员账号：person/person  

#### 前端运行

1、下载包：npm install

2、配置代理（vue.config.js）

```
    proxy: {
      '/api': {
        target: 'http://127.0.0.1:8101',
        changeOrigin: true,
        pathRewrite: {
          '^/api': ''
        }
      },
      '/exam': {
        target: 'http://127.0.0.1:8101',
        changeOrigin: true,
        pathRewrite: {
          '^/exam': ''
        }
      }
    }
```

3、运行：npm run dev

# 界面
![输入图片说明](https://images.gitee.com/uploads/images/2020/1207/173238_e6c22c67_2189748.jpeg "17-32-10.jpg")
![主界面](https://images.gitee.com/uploads/images/2020/1019/182239_4a87af30_2189748.jpeg "222.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/182532_04c42741_2189748.jpeg "444.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/182543_44dcc2d7_2189748.jpeg "555.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/182551_4d404492_2189748.jpeg "666.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/183109_fdc30de8_2189748.jpeg "777.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/183117_30b44530_2189748.jpeg "888.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/183023_2f3baeb9_2189748.jpeg "999.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/183032_f5016335_2189748.jpeg "1010.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/183040_38fd74ed_2189748.jpeg "1111.jpg")
![输入图片说明](https://images.gitee.com/uploads/images/2020/1019/183047_a31619cd_2189748.jpeg "1212.jpg")
