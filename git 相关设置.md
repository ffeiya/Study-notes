# git 相关设置

## 1、 问题合集
### 1.1 gitee push 文件时需要输入用户名与密码

问题与使用的是http方式来推送，关于推送方式可以使用以下命令查看
```shell
git remote -v
```

需要重新配置origin的地址
```shell
git remote rm origin 

git remote add origin [ssh 仓库地址]
```
