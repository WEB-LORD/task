## git 的使用

#### 第一次配置 git 需要配置 username email

> paste 粘贴
> 桌面点击右键 --> git bash

1. git config --global user.name "ruanye"
2. git config --global user.email "55343581@qq.com"

### git 仓库提交的流程

> git bash 要在你提交的文件夹下面运行

#初始化 git 仓库 
  --初始化
        git init  一个仓库只需要初始化一次
  --添加文件到缓存区
        git add 文件名
        通常使用全部添加
        git add -A -A 表示 all 的意思 所有(git add \*)

  --提交文件到本地仓库（自己电脑）
        git commit -m'第一次提交'       -m 通常表示你此次提交内容的备注

  --添加远程仓库  
        git remote add  
        origin 仓库名  
            https://github.com/ruanye/1808B.git 仓库地址
        git remote add origin https://github.com/ruanye/1808B.git

  --查看远程仓库地址
        git remote -v

  --推送代码到远程仓库  
        git push origin master

### 删除远程仓库

git remote rm origin

- 同一个仓库/项目

#### 如果是第一次提交 5 步

1. git init
2. git add -A
3. git commit -m'你的注释'
4. git remote add 仓库地址 添加远程仓库(第一次提交时候使用)
5. git push origin master

#### 如果有修改 第二、第三.....第 n 次 3 步

1. git add -A
2. git commit -m'注释'
3. git push origin master


#### 第一次提交的示例

1. git init
2. git add -A //添加上传的内容
3. git commit -m "VUE" //告诉云盘你传的是视频还是图片
4. git remote add origin https://github.com/ruanye/1808vue.git 存储的文件夹
5. git push -u origin master 上传按钮

### 拷贝仓库地址到本地

下载 git clone +仓库地址
例子：git clone https://github.com/ruanye/1807lesson.git

### 合作做项目或者远程仓库有更改这时每次提交（commit）之前必须 git pull origin master (拉取远程仓库) 为了保证同步
git pull origin master (拉取远程仓库)







## node 的基础知识

nodejs 后端语言 java/php 等价 单线程/异步，无阻塞 i/o

### node 的几个核心模块

1. http 模块 创建服务器
   新建文件 app.js
2. url 模块 解析 url
3. path 模块 解析路径 path.join path.resolve
4. fs filesystem 文件处理 读写文件

### node 的启动方式

1. vscode 插件 code runner
2. node + 文件名
3. 服务端代码有改动需要重启

### node 模块的使用 commonjs 规范

moulde.exports 表示导出模块
require 引入模块

- window 常用 linux 命令  
  touch 建立文件
  mkdir 新建文件夹
  cd 进入文件路径





####vue
### 一）package.json的作用(了解)
- node_moudules 文件夹 -->放着我们项目的依赖 
- dependencies(依赖)  devDependencies(开发依赖) 写代码的时候需要用，打包的时候不需要 npm install 其实就是走的依赖 
- scripts 脚本 npm run serve 
- name 项目名称, version:版本号
### 二）路由懒加载（掌握2，3）
1. /* webpackChunkName: "about" */   可以给懒加载模块起名 
2. import() 表示懒加载，es6的语法 
3. 路由懒加载的写法  
```js
() => import('./views/Home.vue')
``` 
## 流程
### 一） 项目的目录结构
- mock  如果自己写模拟数据创建mock文件夹
- src
 - view         页面级组件
 - libs         工具类 util.isArray 
 - componments  基础组件/公共组件 
 - api          放ajax请求 
    - index.js
### 二) 项目的页面 首页 列表 购物车  个人中心 详情页 
1）app.vue 配置router-link 配置导航  
2）views 里面建页面组件 List.vue  Car.vue Profile.vue  Detail.vue 	