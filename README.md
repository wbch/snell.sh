# Snell 安装脚本

大概也许应该有可能支持自定义端口吧，Centos7上测试可行。

## 安装


Debian & Ubuntu 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/ydzydzydz/snell.sh/master/snell-port.sh
chmod +x snell.sh
./snell.sh
```

Centos & RedHat 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/ydzydzydz/snell.sh/master/snell.centos-port.sh
chmod +x snell.sh
./snell.sh
```

**默认端口号`12312`，如需修改请安装  Snell  时输入端口号**



## 卸载

卸载方法：

```
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/ydzydzydz/snell.sh/master/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```



## 查看

运行状态

```
systemctl status snell
```

重启 Snell
```
systemctl restart snell
```

启动 Snell
```
systemctl start snell
```

停止 Snell
```
systemctl stop snell
```



## 捷径

照着大佬的脚本撸了个捷径，直接运行即可安装&卸载&查看

但是不能自定义端口，默认端口为`13254`，安装结束后会将 Snell 配置导出到备忘录，复制到 Surge 中即可使用



## 修改

查看 Snell 配置文件

```
cat /etc/snell/snell-server.conf
```

修改  Snell 配置文件

```
vi /etc/snell/snell-server.conf
```

vi 编辑如下配置即可

```
[snell-server]
listen = 0.0.0.0:12312
psk = x3IBaVj9K6a6PAzF
obfs = tls
```



---

**Forked from：[primovist/snell.sh](https://github.com/primovist/snell.sh)**

