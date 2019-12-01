@[TOC](Socket连接报错)
ConnectionRefusedError
TimeoutError
# 报错信息：

本次的主要目的是通过python中的socket连接来判断主机是否存活。
TCP连接需要经过三次握手过程，只有经过三次握手建立通信主机之间才能进行信息的发送。
UDP是一个尽最大努力交付的协议，它只关注信息的发送而不在意结果，所以有不确定性。

## ConnectionRefusedError
![ConnectionRefusedError报错信息](https://img-blog.csdnimg.cn/20191201173757421.png)
[WinError 10061] 由于目标计算机积极拒绝，无法连接。
这个是TCP连接目标被拒绝时爆出的错误，也就是目标主机拒绝建立连接。


## TimeoutError
![TimeoutError报错信息](https://img-blog.csdnimg.cn/20191201173837402.png)
[WinError 10060] 由于连接方在一段时间后没有正确答复或连接的主机没有反应，连接尝试失败。
这个是TCP连接目标未得到反应时爆出的错误，即对方不搭理你，skr~。




## 主要代码


```javascript
tcp_ip = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        try:
            tcp_ip.connect((self.ip_str, 8080))
        except ConnectionRefusedError:
			print("目标主机存活!")
        except:
            print("目标主机未存活!")
```

 [1]: http://www.fangdonga.xyz/
 [2]: https://github.com/1337620289/fangdong.github.io
