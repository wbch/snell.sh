# Snell安装脚本

+ [x] 端口：`6333`    可自定义：[1-65535] 
+ [x] PSK：随机生成的16位字符
+ [x] ipv6：`false`    可自定义：[false/true]
+ [x] 若已安装 Snell，直接输出配置

---

### 安装


Debian & Ubuntu 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/ydzydzydz/snell.sh/master/snell-port.sh
chmod +x snell.sh
./snell.sh
```

Centos & RedHat 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/wbch/snell.sh/master/snell.centos.sh
chmod +x snell.sh
./snell.sh
```

---

### 卸载

卸载方法：

```
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/ydzydzydz/snell.sh/master/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```

---

### 查看

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

---

### 修改

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
listen = 0.0.0.0:6333
psk = RANDOM_KEY_HERE
ipv6 = false
```

---

**Forked from：[primovist/snell.sh](https://github.com/primovist/snell.sh)**

