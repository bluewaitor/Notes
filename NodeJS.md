# NodeJS学习笔记

## Node安装

到[nodejs官网][nodejs]下载最新版本的nodejs,傻瓜式安装,不赘述.  
完成之后用`node -v`命令查看版本,如果显示则说明安装成功.  
配置npm安装全局module和cache两个目录,用下面两个命令:  

    npm config set prefix "D:\nodejs\node_global"
    npm config set cache "D:\nodejs\node_cache"

将`D:\nodejs\node_global`加入系统环境变量path,就能在任何地方使用全局module的命令了.

## npm命令

- npm install [-g] [modulename[@version]] (安装module,可以跟上版本,比如jade@1.8.0,-g没写就是安装在当前目录下,如果没写modulename则会在当前目录查找package.json文件,然后根据这个文件里面的信息安装所需的module)
- npm rm(r,uninstall,un) [-g] modulename[@version] (删除module,-g没写会在当前目录下寻找module)
- npm update modulename (更新module)
- npm list(ls,la,ll) (查看装了什么module)
- npm config (在上面有用过了,用来配置的)
- npm docs(home) modulename (打开module的主页)
- npm init (引导我们生成一个package.json文件)

更多参考[npm官网][npmdoc]

## bower命令

- `bower cache <command> [<args>]` (管理bower的缓存)
- `bower cache clean <name>#<version> [<name>#<version> ..]` (清除缓存)
- `bower cache list <name> [<name> ...]` (列表显示bower的缓存)
- `bower help <command>` \<command>(显示关于bower的帮助信息)
- `bower home <package>#<version>` (用默认浏览器打开包名的官网,没写包名则在打开当前目录下包名的官网,如果不在package下,则会报错)
- `bower info <package>#<version> [<property>]` 显示所有包的信息
- `bower init` 创建一个bower.json
- `bower install <endpoint> [<endpoint> ..] [<options>]` 安装包
  - `-F, --force-latest:` Force latest version on conflict(冲突的时候用最新的版本)
  - `-p, --production:` Do not install project devDependencies(不安装在开发依赖)
  - `-S, --save:` Save installed packages into the project’s bower.json dependencies(把下载下来的package写入项目的bower.json文件的项目依赖中)
  - `-D, --save-dev:` Save installed packages into the project’s bower.json devDependencies(同上,只不过是把它写入开发依赖中)
- `bower link <name> [<local name>]` (在本地bower库建立一个项目链接)
- `bower list [<options>]` 把下载的packages列出来,会检查版本的更新
  - -p, --paths: Generates a simple JSON source mapping
  - -r, --relative: Make paths relative to the directory config property, which defaults to bower_components
- `bower lookup <name>` (通过包名查看URL)
- `bower prune` (移除本地多余的包)
- `bower register <name> <url>` (注册一个包)
- `bower search <name>` (找到所有的包或者特定的包)
- `bower update <name> [<name> ..] [<options>]` (根据bower.json将所安装的包升级到可升级的最新版本)
  - -F, --force-latest: Force latest version on conflict
  - -p, --production: Do not install project devDependencies
- `bower uninstall <name> [<name> ..] [<options>]` (从bower_components目录将包删掉)
  - -S, --save: Remove uninstalled packages from the project’s bower.json dependencies
  - -D, --save-dev: Remove uninstalled packages from the project’s bower.json devDependencies
- `bower version [<newversion> | major | minor | patch]` (Run this in a package directory to bump the version and write the new data back to the bower.json file.)
  - -m, --message: Custom git commit and tag message

参考[bower官网的api][bowerdoc]

## Grunt命令

    CLI（command-line interface，命令行界面）

[nodejs]:www.nodejs.org
[npmdoc]:https://docs.npmjs.com/cli/
[bowerdoc]:http://bower.io/docs/api/