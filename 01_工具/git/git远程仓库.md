1. 启动ssh代理

    eval `ssh-agent -s`

2. 生成秘钥

    `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` 

    这里需要把这个换成自己的邮箱，如果需要指定名称，使用如下命令

    `ssh-keygen -t rsa -b 4096 -C "wym_sugarcane@163.com" -f '~/.ssh/id_rsa_163email'`

3. 将公钥复制到github/gitlab

    登录到你的GitLab账户,进入 "Settings" -> "SSH Keys",点击 "Add SSH Key",将你的公钥粘贴到 "Key" 字段,并给它一个标题。

4. 测试能否联通

    `ssh -T git@github.com`

    如果不行，则检查秘钥的权限是否为600/644，不是的话修改一下

    chmod 600 ~/.ssh/id_rsa 

    chmod 644 ~/.ssh/id_rsa .pub

    如果还是不行，在~/.ssh下找到config文件，没有的话则创建，填入

    ```tex
    Host github.com
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_rsa
    
    ```

5. 克隆代码即可

    `git clone git@gitlab.com:username/repository.git`
