
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
- 首先git clone 网站地址
- 之后代码有更新，再通过git pull拉取更新
### 我不会玩了一次就一直想着玩吧!那就挺难受的.