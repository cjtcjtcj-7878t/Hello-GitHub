
# 个人笔记理解

## Markdown还是比较好用的

### 对于计算机学生来说，Markdown格式是有必要掌握的一种文件格式
- ~ 表示“家目录”，/Users/shoushui

- / 表示“根目录”

- cd .. 返回上一级目录

- cd / 返回根目录

- cd ~ 返回家目录

- touch 创建文件

- rm 删除文件（谨慎使用）

- mkdir 创建文件夹

- rmdir 删除文件夹（谨慎使用）

- cd 进入某个文件夹

- cat 打印文件内容

- clear 清空终端内容
-  按下方向键“上键”可以快速查找历史使用的终端命令，提高效率

- git init"初始化一个git空的仓库"
- git status"查看当前目录下文件的跟踪状态"
- git add 文件名 "增加需要git管理的文件"
- git add . "将目录下所有文件纳入git版本管理"
- git commit -m "将追踪的文件放入暂存区"
- git log --oneline "查看commit历史,前面的序列号有用处"
- git checkout 序列号 "将文件回溯到某个commit版本"
- git checkout main "将文件回溯到最新commit版本"

### 当某个文件发生更新：
- git add 文件名
- git commit -m "说明" 将变更的地方提交到暂存区

### 本地仓库与github远程仓库关联
- 首先本地某个文件夹内需要先创建git仓库
- 首先在github平台new repository 进入命令行提示界面（本机已经完成ssh链接github）(创建仓库时不允许平台自动添加README.md以及.gitignore)
- 以上两步完成后，进入本地仓库目录
- 正确敲出相关命令
- 本地仓库与远程仓库关联后，就是相对固定的命令

### 在一个新计算机上拉取github代码
- 确保git已经安装
- 首先git clone 完整URL.git
- 之后代码有更新，再通过git pull拉取更新

### python碎碎念
- python有多个可安装版本，再加上它丰富的第三方库，使得python版本管理是一门学问
- 在Macbook终端中使用python3 --version 可查看当前电脑安装的python版本，另外前面提过多个不同版本的python可以共存与同一台计算机，在多个版本基础上
使用which -a python3 可查看所有已经安装的python的绝对路径
- 输入完整的python安装路径后 --version就可以查看该路径安装的python版本。
- 前言：不同版本的python可以共存一台计算机，同时各个版本的python都可以各自安装第三方库，各个版本的python安装的同一个第三方库的版本也会有差异，一个python项目需要特定的python环境，这种背景下，为每个python项目做好环境管理也是一门学问。避免所有项目都使用同一个python环境。
- 可以通过.venv,anaconda管理不同版本的python。
- 每一个python项目创建一个.venv虚拟环境，用于管理python版本、第三方库版本。
## 创建.venv虚拟环境步骤：
- cd 进入项目目录
- python() -m venv (--prompt=) .venv 括号可写python版本，第二个括号内容可有可无，主要是给虚拟环境起名。
- source .venv/bin/activate 激活当前虚拟环境，激活成功后命令行前方出现括号，括号内容是当前虚拟环境的名称。
- 之后就可以通过pip命令为当前的python环境安装第三方库以及使用pip命令。
- 通过deactivate退出当前虚拟环境。
## 新环境
- 不过.venv不会被git跟踪。需要额外生成文件记录使用的库--requirements.txt,方便其他计算机环境进行安装配置。
- 通过source .venv/bin/activate 进入虚拟环境。
- pip freeze > requirements.txt 创建requirements.txt文件。
- 对于新环境的计算机，激活venv环境后，使用pip install -r requirements.txt 就可以安装项目所需要的依赖。

### Linux用户碎碎念
- Linux用户对文件具有r(4),w(2),x(1)三种权限,分别表示读、写、可执行。
- 对于单个文件来说，x(1)-可执行通常意味着文件可以作为程序或脚本进行运行
- 对于文件夹来说，x(1)-可执行通常意味着可以cd进入访问该文件夹,ls查看文件的元数据,cat访问/读取/执行/修改文件夹内的文件
touch、mkdir、rmdir创建文件、创建文件夹、删除文件夹。
- chmod可用于添加或移除权限，数字法设置权限遵循User,Group,Others的顺序。
- u代表User,g代表Group,o代表Others。+表示增加权限，-表示移除权限。 
- 文件夹(目录)最大权限是777，文件最大权限是666。
- 通过umask命令查看当前的默认权限掩码，则创建的文件夹或者文件默认权限就是各自的最大权限(文件夹是777，文件是666)减去这个默认权限掩码。
- 可以通过umask命令改变当前的默认权限掩码，也就改变了文件夹或者文件的默认权限。
### 我不会玩了一次就一直想着玩吧!那就挺难受的.
