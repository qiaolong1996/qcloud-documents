如下操作以 Windows 2012 为例： 
1. 登录云服务器实例，进入操作系统的【控制面板】>【网络和 Internet】>【网络和共享中心】，单击命名为“以太网”的网卡进行编辑。
![](https://main.qcloudimg.com/raw/4696aa941df5c22dbf4446c01aabefbc.png)
2. 在“以太网状态”弹窗中，单击左下角【属性】。
3. 在“以太网属性”弹窗中，选中【Internet 协议版本 6（TCP/IPv6）】并单击【属性】。
![](https://main.qcloudimg.com/raw/1f10d494b792d975a387ec6e38555021.png)
4. 在“Internet 协议版本 6（TCP/IPv6）属性”弹窗中，手工输入云服务器获取到的 IPv6 地址 ( 请参见[搭建 IPv6 私有网络：步骤三](https://cloud.tencent.com/document/product/215/47557)) 并设置 DNS（推荐使用`240c::6666`），单击【确定】。
![](https://main.qcloudimg.com/raw/fac63249f22197686d68e3afffb3eb14.png)
5. 在操作系统界面，选择左下角的<img src="https://main.qcloudimg.com/raw/87d894e564b7e837d9f478298cf2e292.png" style="margin:-3px 0px;width:25px">，单击 <img src="https://main.qcloudimg.com/raw/f0c84862ef30956c201c3e7c85a26eec.png" style="margin: -3px 0px;">，打开 “Windows PowerShell” 窗口，依次执行如下命令配置默认路由以及查看 IPv6 地址。
```
netsh interface ipv6 add route ::/0 "以太网"
ipconfig
```
![](https://main.qcloudimg.com/raw/ba325fb98c4efe86a1f3a4bcd55f77be.png)
