# embyonekey
群辉emby套件版服务端一点五键白嫖
<br>左点点右点点,算你一点五键吧<br>
<br>前提如下 群辉安装好webstation跟emby<br>
<br>没有新建任何虚拟主机<br>
<br>在webstation虚拟主机中按图片中新建虚拟主机<br>
<br><img src="https://github.com/s1oz/embyonekey/blob/master/webstation.png"><br>
<br>然后登录群辉root账户后运行<br>
</p><pre><code>wget -N --no-check-certificate &quot;https://raw.githubusercontent.com/s1oz/embykey/master/embyonekey.sh&quot; &amp;&amp; chmod +x embyonekey.sh &amp;&amp; ./embyonekey.sh
</code></pre><h2>
<br>
<br>
<br>运行完脚本后请将mb3admin劫持到自己nas<br>
<br>如群辉IP为10.0.0.10<br>
<br>op类路由命令为<br>
</p><pre><code>vi /etc/myhosts<br></code></pre><h2>
<br>10.0.0.10 mb3admin.com<br>
</p><pre><code>:wq<br></code></pre><h2>
<br>保存退出后在op中的网络-HOSTS和解析文件-额外的HOSTS文件中加入/etc/myhosts<br>
<br>群辉修改命令为<br>
</p><pre><code>vi /etc/hosts<br></code></pre><h2>
<br>10.0.0.10 mb3admin.com<br>
</p><pre><code>:wq<br></code></pre><h2>
<br>保存退出后<br>
<br>Windows 安卓 ios等客户端都要安装下面这个证书<br>
<br>https://github.com/s1oz/embykey/blob/master/guomi.cer 右键另存为文件名为guomi.cer的文件后安装相应设备上<br>
<br>IOS需要安装后在设置--通用--关于手机--证书信任设置中把信任证书<br>
  
  
<br>感谢 时光轴 星辰 不会魔法的思思 教程引路<br>
  
