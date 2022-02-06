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

``` powershell
$env:SCOOP='D:\Applications\Scoop'
$env:SCOOP_GLOBAL='D:\Applications\Scoop\ScoopGlobalApps'
```