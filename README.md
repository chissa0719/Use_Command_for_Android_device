# Use_Command_for_Android_device

Android端末からpingとか打ちたかったので，少し勉強してみた<br>
<br>

## shellからの実行

純粋なコマンドの実行は大体これ<br>
<br>

```
# adb shell ping 192.168.0.1
PING 192.168.0.1 (192.168.0.1) 56(84) bytes of data.
64 bytes from 192.168.0.1: icmp_seq=1 ttl=64 time=27.2 ms
64 bytes from 192.168.0.1: icmp_seq=2 ttl=64 time=27.8 ms
64 bytes from 192.168.0.1: icmp_seq=2 ttl=64 time=28.4 ms (DUP!)
64 bytes from 192.168.0.1: icmp_seq=3 ttl=64 time=28.1 ms
64 bytes from 192.168.0.1: icmp_seq=3 ttl=64 time=28.1 ms (DUP!)

# adb shell ls -a
.
..
acct
apex
bin
(続く)
```

## 何かしらのinstall

```
# adb install (package_name).apk
# adb install (package_name).apex
```
<br>
