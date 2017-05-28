1. 生成密匙对

```bash
$ ssh-keygen -t rsa -C "your-email@youemail.com"  #-t密钥类型，默认rsa，-C注释文字，比如邮箱
```

2. 添加公匙到github账户

```bash
$ ssh -T git@github.com  #测试SSH连接
```

3. 修改本地ssh remote url

```bash
$ git remote -v  #查看远程地址
$ git remote set-url origin git@github.com:someaccount/someproject.git  #更换目前远程访问地址
```



