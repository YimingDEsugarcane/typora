```
git 

1. 启动SSH代理:
eval `ssh-agent -s`

2. 生成秘钥
ssh-keygen -t rsa -b 4096 -C "your_email@example.com" 这里需要把这个换成自己的邮箱
位置在 ~/.ssh下

3. 将公钥放到gitlab
登录到你的GitLab账户,进入 "Settings" -> "SSH Keys",点击 "Add SSH Key",将你的公钥粘贴到 "Key" 字段,并给它一个标题。

4. git clone git@gitlab.com:username/repository.git
git clone http://219.134.161.162:8888/yimingwu/allsaints_base.git

5. 拉取代码
git pull
```

