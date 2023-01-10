# （实验性功能）服务器切换

## 版本需求

这个功能需要 TestFlight 62 以上的版本，尚未正式发布安卓端。

## 使用方式

当处于登陆页面时，可以在用户名文字框内输入服务器切换指令，然后登陆，结果会返回在登陆框中。

### 服务器切换指令

```
ss{新的服务器信息}
```

不包括花括号。

### 服务器信息

服务器信息为 JSON 格式 Base64 编码后的字符串。

Base64 编码前格式如下，不支持 JSON5 格式，需要把注释删除，URL地址后的斜线关系到数据请求的成功与否，注意检查。

```json5
{
    // 服务器ID，用于定位服务器资源的本地位置。
    // 建议符合：所有小写字母和数字
    "ServerId": "explode",
    // 服务器 Graphql 后端地址
    "ServerGraphqlBackend": "http://example.com:10483/graphql",
    // 服务器资源下载地址
    "ServerResourceDownloadBase": "http://example.com:10483",
    // 服务器多人联机 PhotonMaster 服务器地址
    "ServerPhotonMasterAddress": null
}
```

## 可用的服务器切换指令

已经添加了 `ss`，直接复制粘贴即可用。

### Explode

```
ssewogICAgIlNlcnZlcklkIjogImV4cGxvZGUiLAogICAgIlNlcnZlckdyYXBocWxCYWNrZW5kIjogImh0dHA6Ly80My4xNDIuMTczLjYzOjEwNDgzL2dyYXBocWwiLAogICAgIlNlcnZlclJlc291cmNlRG93bmxvYWRCYXNlIjogImh0dHA6Ly80My4xNDIuMTczLjYzOjEwNDgzIiwKICAgICJTZXJ2ZXJQaG90b25NYXN0ZXJBZGRyZXNzIjogIjQzLjE0Mi4xNzMuNjM6NDUzMCIKfQ==
```

### Reboot

```
ssewogICAgIlNlcnZlcklkIjogInJlYm9vdCIsCiAgICAiU2VydmVyR3JhcGhxbEJhY2tlbmQiOiAiaHR0cDovLzEyNC4yMjIuMTMzLjY2OjIwNDQzL2dyYXBocWwiLAogICAgIlNlcnZlclJlc291cmNlRG93bmxvYWRCYXNlIjogImh0dHA6Ly8xMjQuMjIyLjEzMy42NjoyMDQ0MiIsCiAgICAiU2VydmVyUGhvdG9uTWFzdGVyQWRkcmVzcyI6IG51bGwKfQ==
```

如果您有宣传的需要，可以在 [Dyfused/dyfused.githuo.io](https://github.com/Dyfused/dyfused.github.io) 提交 Issue 或 PullRequest。