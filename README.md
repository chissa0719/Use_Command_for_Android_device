# Use_Command_for_Android_device

Android端末からpingとか打ちたかったので，少し勉強してみた<br>
<br>

## shellからの実行

純粋なコマンドの実行は大体これ<br>

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

## 特定Webページを開く

https通信そもそもできてる？って確認やIPアドレス宛の時は便利かも<br>

```
# adb shell am start -a android.intent.action.VIEW -d "https://192.168.0.1"
```

## 何かしらのinstall

もともとパッケージがあるものはこれで入るけど，```curl```みたいにパッケージがないものは<br>
バイナリから拾っていこないとダメっぽい<br>

```
# adb install (package_name).apk
# adb install (package_name).apex
```

## 参考

- 開発者オプションの設定<br>
https://www.uubyte.com/ja/how-to-use-ping-command-on-android.html

- adbコマンド集<br>
https://qiita.com/t2low/items/cb37cec5f864c4748e14

<br>
