# Scoop windows 安装与配置

## 1、Scoop安装
```shell
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')

# or shorter
iwr -useb get.scoop.sh | iex
```

可能会碰到powershell的组权限问题

```shell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
```

设置环境变量，安装到自定义目录
``` powershell
$env:SCOOP='D:\Applications\Scoop'
[Environment]::SetEnvironmentVariable('SCOOP',$env:SCOOP,'User')

$env:SCOOP_GLOBAL='D:\Applications\Scoop\ScoopGlobalApps'
[Environment]::SetEnvironmentVariable('SCOOP_GLOBAL',$env:SCOOP_GLOBAL,'User')

```

设置代理
```powershell

scoop config proxy 127.0.0.1:{port}

```