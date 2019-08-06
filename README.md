# SS-Collection

常用资源汇集，仅个人收集向

## App

### Shadowsocks

| Platform | Releases                                                                                       |
| -------- | ---------------------------------------------------------------------------------------------- |
| Windows  | [shadowsocks/shadowsocks-windows](https://github.com/shadowsocks/shadowsocks-windows/releases) |
| MacOS    | [shadowsocks/ShadowsocksX-NG](https://github.com/shadowsocks/ShadowsocksX-NG/releases)         |
| Android  | [shadowsocks/shadowsocks-android](https://github.com/shadowsocks/shadowsocks-android/releases) |
| obfs     | [shadowsocks/simple-obfs-android](https://github.com/shadowsocks/simple-obfs-android/releases) |

### ShadowsocksR

[协议插件文档](https://github.com/shadowsocksr-backup/shadowsocks-rss/blob/master/ssr.md)

| Platform | Releases                                                                                                         |
| -------- | ---------------------------------------------------------------------------------------------------------------- |
| Windows  | [shadowsocksr-backup/shadowsocksr-csharp](https://github.com/shadowsocksr-backup/shadowsocksr-csharp/releases)   |
| MacOS    | [shadowsocksr-backup/ShadowsocksX-NG](https://github.com/shadowsocksr-backup/ShadowsocksX-NG/releases)           |
| Android  | [shadowsocksr-backup/shadowsocksr-android](https://github.com/shadowsocksr-backup/shadowsocksr-android/releases) |

### ShadowsocksRR

[协议插件文档](https://github.com/shadowsocksrr/shadowsocks-rss/blob/master/ssr.md)

| Platform | Releases                                                                                             |
| -------- | ---------------------------------------------------------------------------------------------------- |
| Windows  | [shadowsocksrr/shadowsocksr-csharp](https://github.com/shadowsocksrr/shadowsocksr-csharp/releases)   |
| Android  | [shadowsocksrr/shadowsocksr-android](https://github.com/shadowsocksrr/shadowsocksr-android/releases) |

### SSTap

[Official website](https://www.sockscap64.com/sstap-enjoy-gaming-enjoy-sstap/)

| Version | Download                                                                                                                       |
| ------- | ------------------------------------------------------------------------------------------------------------------------------ |
| 1.0.9.7 | [SSTap-beta-setup-1.0.9.7.zip](https://github.com/Tsuk1ko/SS-and-SSR-Collection/raw/master/SSTap/SSTap-beta-setup-1.0.9.7.zip) |
| 1.1.0.1 | [SSTap-beta-setup-1.1.0.1.zip](https://github.com/Tsuk1ko/SS-and-SSR-Collection/raw/master/SSTap/SSTap-beta-setup-1.1.0.1.zip) |

Rules: [FQrabbit/SSTap-Rule](https://github.com/FQrabbit/SSTap-Rule)

## Rules

| Type      | Repositories                                                                        |
| --------- | ----------------------------------------------------------------------------------- |
| AutoProxy | [gfwlist/gfwlist](https://github.com/gfwlist/gfwlist)                               |
| DNSMasq   | [felixonmars/dnsmasq-china-list](https://github.com/felixonmars/dnsmasq-china-list) |
| PAC       | [breakwa11/gfw_whitelist](https://github.com/breakwa11/gfw_whitelist)               |

### Get a domain list from gfwlist

From [改华硕[N14U N54U]5G 2G的7620老毛子Padavan固件](https://www.right.com.cn/forum/thread-161324-1-1.html)

```bash
curl https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt | base64 -d | sort -u | sed '/^$\|@@/d' | sed 's#!.\+##; s#|##g; s#@##g; s#http:\/\/##; s#https:\/\/##;' | sed '/^[0-9]\+\.[0-9]\+\.[0-9]\+\.[0-9]\+$/d' | grep '^[0-9a-zA-Z\.-]\+$' | grep '\.' | sed 's#^\.\+##' | sort -u > gfwlist_domain.txt
```

## CHNRoutes

### IPIP.NET

[17mon/china_ip_list](https://github.com/17mon/china_ip_list)

### APNIC

```bash
curl 'http://ftp.apnic.net/apnic/stats/apnic/delegated-apnic-latest' | grep ipv4 | grep CN | awk -F\| '{ printf("%s/%d\n", $4, 32-log($5)/log(2)) }' > chnroute.txt
```

## DNS Server

| Repositories                                                                  | Language | Platform           |
| ----------------------------------------------------------------------------- | -------- | ------------------ |
| [shadowsocks/ChinaDNS](https://github.com/shadowsocks/ChinaDNS)               | C        | All                |
| [shadowsocks/ChinaDNS-Python](https://github.com/shadowsocks/ChinaDNS-Python) | Python   | All                |
| [chengr28/Pcap_DNSProxy](https://github.com/chengr28/Pcap_DNSProxy)           | C++      | All                |
| [shawn1m/overture](https://github.com/shawn1m/overture)                       | Go       | All                |
| [bitbeans/SimpleDnsCrypt](https://github.com/bitbeans/SimpleDnsCrypt)         | C#       | Windows (with GUI) |
