# fish-v4-entrypoint


# 子git

```
git submodule add https://joyanhui:XXX@github.com/joyanhui/fish-v4-entrypoint.git   server-go/_config/fish-v4-entrypoint
```


## 放github 
不用绑定域名
https://joyanhui.github.io/fish-v4-entrypoint/dev-v4.json
cdn 要打开 302跟随
http://entrypoint.cf-cdn-ns.work/fish-v4-entrypoint/dev-v4.json

另外 cdn 要打开   
-  因为github  所以 走 ipv6
- 回源跟随301/302配置 打开
- 通过对单IP单节点QPS限制   500
- 合并回源配置 打开 
- 用量封顶配置  瞬间 5分钟 500M  404  ，以及 告警阈值 流量的80%
- 离线缓存配置  防止被墙
- post限制  1M

## 放对象储存
放 对象储存，阿里云的只能公共读库，会被刷。 


腾讯云倒是支持私有库，那么 改为 ，用 阿里云 私有 oss ，腾讯  云cdn

 https://joyanhui.github.io/fish-v4-entrypoint/  不绑定域名

https://joyanhui.github.io/fish-v4-entrypoint/dev-v4.json


