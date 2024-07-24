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

仅支持 JSON，不可使用 `//` 注释，如果使用了下面的模板，请删除注释后使用。

```json5
{
    // 服务器ID - 用于定位本地资源的名称
    // 不能包含当前系统不允许出现在路径里的字符，例如 '<' 不能出现在 Windows 里
    // 建议仅使用英文大小写和数字
    "ServerId": "Explode",
    // 后端地址 - 服务器地址
    "ServerGraphqlBackend": "http://34.92.242.92:10443/graphql",
    // 资源地址 - 访问和下载游戏数据的根地址
    "ServerResourceDownloadBase": "http://34.92.242.92:10443",
    // 联机服务器地址 - 处理联机相关事务的服务器地址
    "ServerPhotonMasterAddress": null
}
```
