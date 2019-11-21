### 功能
下载gfwlist并且将结果插入adguard的配置文件(/usr/bin/AdGuardHome/AdGuardHome.yaml)中，对gfwlist的所有域名进行tcp://208.67.220.220#5353 的查询，并且进行 `/etc/init.d/AdGuardHome restart`<br>
### 用法
编辑 /usr/bin/AdGuardHome/AdGuardHome.yaml 在upstream_dns: 下面的行中加入两行（没有反斜杠）<br>
```
  - '\''[/programaddstart/]#'\''
  - '\''[/programaddend/]#'\''
```
使用contab定时运行gfw2adg.sh即可自动更新<br>
