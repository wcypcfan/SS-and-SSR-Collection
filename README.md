# SS-and-SSR-Collection
仅个人收集向，不定时更新

## Source
### Shadowsocks
| Platform | URL                                                         |
|----------|-------------------------------------------------------------|
| Windows  | https://github.com/shadowsocks/shadowsocks-windows/releases |
| MacOS    | https://github.com/shadowsocks/ShadowsocksX-NG/releases     |
| Android  | https://github.com/shadowsocks/shadowsocks-android/releases |
| obfs     | https://github.com/shadowsocks/simple-obfs-android/releases |

### ShadowsocksR
| Platform | URL                                                                  |
|----------|----------------------------------------------------------------------|
| Windows  | https://github.com/shadowsocksr-backup/shadowsocksr-csharp/releases  |
| MacOS    | https://github.com/shadowsocksr-backup/ShadowsocksX-NG/releases      |
| Android  | https://github.com/shadowsocksr-backup/shadowsocksr-android/releases |

### SSTap
https://www.sockscap64.com/sstap-enjoy-gaming-enjoy-sstap/

### PAC
https://github.com/breakwa11/gfw_whitelist

### chnrouter
```bash
curl 'http://ftp.apnic.net/apnic/stats/apnic/delegated-apnic-latest' | grep ipv4 | grep CN | awk -F\| '{ printf("%s/%d\n", $4, 32-log($5)/log(2)) }' > chnroute.txt
```
