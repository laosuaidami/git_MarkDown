# git_MarkDown
[廖雪峰git教程]
## 设置别名
    ci = commit  
	br = branch  
	lg = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short  
	st = status  
	
## 逐行查看文件的修改历史
- git blame (file name)  

- 从第 100 行开始，到 110 行。逐行查看文件的修改历史  
git blame –L 100,110 (file name) 


## git clean 使用
- 列出打算清除的档案  
git clean -n

- 真正的删除  
git clean –f

- 连 .gitignore 中忽略的档案也清除  
git clean -x


## Commit message 和 Change log 编写([Angular规范])
1. **Commit message 的作用**
2. **Commit message 的格式**
    - **每次提交，Commit message 都包括三个部分：Header，Body 和 Footer。**  
    ![][格式图片]
    其中，Header 是必需的，Body 和 Footer 可以省略。
不管是哪一个部分，任何一行都不得超过72个字符（或100个字符）。这是为了避免自动换行影响美观。
    1. Header  
    Header部分只有一行，包括三个字段：type（必需）、scope（可选）和subject（必需）。  
        - type  
        type用于说明 commit 的类别，只允许使用下面7个标识。
        ![][type_form]
        如果type为feat和fix，则该 commit 将肯定出现在 Change log 之中。其他情况（docs、chore、style、refactor、test）由你决定，要不要放入 Change log，建议是不要。  
        - scope  
scope用于说明 commit 影响的范围，比如数据层、控制层、视图层等等，视项目不同而不同。
        - subject  
subject是 commit 目的的简短描述，不超过50个字符。  
             - [x] 以动词开头，使用第一人称现在时，比如change，而不是changed或changes
             - [x] 第一个字母小写
             - [x] 结尾不加句号（.）
> 详见[阮一峰的网络日志]

## 信息查看
- short and branch  
git status -sb

- 查看某个提交信息  
git show HEAD

- 查看提交历史  
git log  (file name)  
git log --grep (msg) 
git log -n  


## git diff
![][git_diff]


## 回撤操作



<!--- 下面是本文本用到的链接 -->

[Angular规范]: https://docs.google.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#heading=h.greljkmo14y0
[阮一峰的网络日志]: http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html
[格式图片]: images/message_form.png
[type_form]: images/type_form.png
[git_diff]: images/git_diff.png
[廖雪峰git教程]: https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000

