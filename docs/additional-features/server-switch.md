---
title: 服务器切换
---

!!! example "版本需求"

    需要 Dyfused 1.0.2(69) 以上的版本

```
ss{转服码}
```

## 现有转服码

最后更新：2023/9/15

``` title="Explode"
ssewogICAgIlNlcnZlcklkIjogIkV4cGxvZGUiLAogICAgIlNlcnZlckdyYXBocWxCYWNrZW5kIjogImh0dHA6Ly8zNC45Mi4yNDIuOTI6MTA0NDMvZ3JhcGhxbCIsCiAgICAiU2VydmVyUmVzb3VyY2VEb3dubG9hZEJhc2UiOiAiaHR0cDovLzM0LjkyLjI0Mi45MjoxMDQ0MyIsCiAgICAiU2VydmVyUGhvdG9uTWFzdGVyQWRkcmVzcyI6IG51bGwKfQ==
```

``` title="Dynamite: Reboot"
ssewogICAgIlNlcnZlcklkIjogInJlYm9vdCIsCiAgICAiU2VydmVyR3JhcGhxbEJhY2tlbmQiOiAiaHR0cDovLzEyNC4yMjIuMTMzLjY2OjIwNDQzL2dyYXBocWwiLAogICAgIlNlcnZlclJlc291cmNlRG93bmxvYWRCYXNlIjogImh0dHA6Ly8xMjQuMjIyLjEzMy42NjoyMDQ0MiIsCiAgICAiU2VydmVyUGhvdG9uTWFzdGVyQWRkcmVzcyI6IG51bGwKfQ==
```

## 关于转服码

转服码为包含数据的 JSON 格式文档使用 Base64 编码后的字符串。

#### 未编码转服码格式

仅支持 JSON，不可使用 `//` 注释。

```json5
{
    // 配置版本
    "ConfigVersion": 1,
    // 旧版遗留字段
    "GraphQl": null,
    // 旧版遗留字段
    "Resource": null,
    // 旧版遗留字段
    "PhotonMaster": null,
    // 当前服务器信息
    "ServerInfo": {
        // 服务器 ID
        "ServerId": "Explode",
        // 服务器后端 GraphQL 地址
        "ServerGraphqlBackend": "http://example.com:10443/graphql",
        // 服务器资源下载地址
        "ServerResourceDownloadBase": "http://example.com:10443",
        // 服务器多人联机 PhotonMaster 地址
        "ServerPhotonMasterAddress": "example.com:4530",
        // 服务器登录信息
        // [REDACTED] 为已经抹除的信息，默认该字段是加密的，
        // 请不要泄露给他人！
        "Properties": {
            "LastLoginUsername": "[REDACTED]",
            "LastLoginPassword": "[REDACTED]"
        }
    }
}
```