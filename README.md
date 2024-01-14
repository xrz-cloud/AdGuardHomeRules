# AdGuardHomeRules

## `cloudflare.txt` 规则
原理:   
对 `dns` `sni` `dns+sni` 类型的干扰，可由DoH解决。  
- `dns`: DoT/DoH/DoQ
- `sni`: 当DoH启用时，会提前请求目标域名的`HTTPS`的DNS类型获取参数，通过改写该项，启用 `HTTP/3` `ECH` 来防止sni嗅探。

CloudFlare支持Anycast,本规则将部分CF网站重定向至可用IP。  

规则：  
```
https://raw.githubusercontent.com/xrz-cloud/AdGuardHomeRules/main/cloudflare.txt
(下方为镜像)
https://raw.fgit.cf/xrz-cloud/AdGuardHomeRules/main/cloudflare.txt
https://raw.githubusercontents.com/xrz-cloud/AdGuardHomeRules/main/cloudflare.txt
https://cdn.jsdelivr.net/gh/xrz-cloud/AdGuardHomeRules@main/cloudflare.txt
https://fastly.jsdelivr.net/gh/xrz-cloud/AdGuardHomeRules@main/cloudflare.txt
https://gcore.jsdelivr.net/gh/xrz-cloud/AdGuardHomeRules@main/cloudflare.txt
https://raw.githubusercontents.com/xrz-cloud/AdGuardHomeRules/main/cloudflare.txt
https://ghproxy.com/https://raw.githubusercontent.com/xrz-cloud/AdGuardHomeRules/main/cloudflare.txt
https://get.66a.zone/https://raw.githubusercontent.com/xrz-cloud/AdGuardHomeRules/main/cloudflare.txt
```

## picacomic direct connect
原理：pica使用CloudFlare CDN，重写DNS至pica其它域名/CF Anycast IP(可用)即可  
规则：  
```
https://raw.githubusercontent.com/xrz-cloud/AdGuardHomeRules/main/picacomic.txt
(下方为镜像)
https://raw.fgit.cf/xrz-cloud/AdGuardHomeRules/main/picacomic.txt
https://raw.githubusercontents.com/xrz-cloud/AdGuardHomeRules/main/picacomic.txt
https://cdn.jsdelivr.net/gh/xrz-cloud/AdGuardHomeRules@main/picacomic.txt
https://fastly.jsdelivr.net/gh/xrz-cloud/AdGuardHomeRules@main/picacomic.txt
https://gcore.jsdelivr.net/gh/xrz-cloud/AdGuardHomeRules@main/picacomic.txt
https://raw.githubusercontents.com/xrz-cloud/AdGuardHomeRules/main/picacomic.txt
https://ghproxy.com/https://raw.githubusercontent.com/xrz-cloud/AdGuardHomeRules/main/picacomic.txt
https://get.66a.zone/https://raw.githubusercontent.com/xrz-cloud/AdGuardHomeRules/main/picacomic.txt
```
