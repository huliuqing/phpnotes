# 从GitHub克隆版本库提示Permission denied (publickey)错误时，如何解决

操作系统: Windows XP

Git工具 : Git Bash

克隆命令: git clone git@github.com:huliuqing/phpnotes

错误消息:

> Permission denied (publickey)
fatal:Could not read from remote repository

** 解决思路：**

1. 是否设置GitHub SSH公钥信息
2. 如果已设置SSH 公钥信息，确认是不是最新生成的SSH公钥信息

## 解决方案：

### 解决问题1 
如果是未设置SSH公钥信息
step1. 我们需要使用Git工具[生成SSH宻钥数据](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

> 1 打开 Git Bash工具
2 输入命令:  *ssh-keygen -t -ras -b -C 'your_email@examle.com'*
3 当看到"Enter a file in which to save the key"提示消息，*直接按回车键*。
表示使用默认的目录生成宻钥数据
4 当看到
**Enter passphrase (empty for no passphrase): [Type a passphrase]**
**Enter same passphrase again: [Type passphrase again]**
提示时：*输入你的密码*

step2. 将SSH宻钥添加到ssh-agent
> 1 确认ssh-agent是否可用，执行命令: *eval $(ssh-agent -s)*
你将看到"**Agent pid 59566**"提示消息
2将SSH宻钥添加到ssh-agent，执行命令**ssh-add ~/.ssh/id_rsa**

step3 [将SSH宻钥配置到GitHub帐号](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)
>1 将生成的SSH宻钥(id_rsa.pub文件内容)复制到粘贴板
2 进入**GitHub>Setting**选项
3 进入**SSH and GPG keys**选项
4 点击**New SSH key**按钮
5 键入"Title"信息，将id_rsa.pub数据粘贴进**"Key"**
6 点击**Add SSH key**

### 解决问题2 
找到你的id_rsa.pub文件，按照step3的步骤将SSH宻钥配置到GitHub帐号


### 参考资料:
[Git - Permission denied (publickey)](http://stackoverflow.com/a/2643584/1969039)
[Generating a new SSH key and adding it to the ssh-agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
[Adding a new SSH key to your GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)
[github提示Permission denied (publickey)，如何才能解决？](https://www.zhihu.com/question/21402411)