### embyonekey

- 群辉emby套件版服务端一点五键白嫖
- 左点点右点点,算你一点五键吧

# 提前说下
啥也不会瞎捣鼓的
<br/>所以~~~
<br/>请保证在未在Web Station中新建任何虚拟主机
<br/>请按照说明路径正确设置
<br/>出啥问题我也不负责

### 步骤说明
<br/>0. 在群辉中安装好Web Station跟EMBY
<br/>1. 打开Web Station如图所示新建虚拟主机
<br/>![](https://github.com/s1oz/embyonekey/blob/master/webstation.png)




#### 劫持mb3admin伪站

如搭建伪站的NAS地址为10.0.0.10 则如下填写,根据自己实际情况修改

    10.0.0.10 mb3admin.com
	
0. op类路由可以直接在路由中添加额外的hosts文件
<br/>登陆ssh输入以下命令
`vi /etc/myhosts`
<br/>i 进入编辑状态
<br/>输入 `10.0.0.10 mb3admin.com`
`:wq` 保存退出
<br/>登陆op
<br/>点击网络-HOSTS和解析文件-额外的HOSTS文件中加入
`/etc/myhosts`
<br/>保存生效
1. 群辉可以直接登录修改
<br/>登陆ssh输入以下命令
`vi /etc/hosts`
<br/>i 进入编辑状态
<br/>输入 `10.0.0.10 mb3admin.com`
`:wq` 保存退出
2. Windows修改只是路径不同
<br/>直接打开`C:\Windows\System32\drivers\etc\`目录
<br/>修改文件夹中的hosts文件
	
### 接下来运行这条脚本


以root用户执行命令：<br/>
</p><pre><code>wget -N --no-check-certificate "https://raw.githubusercontent.com/s1oz/embyonekey/master/embyonekey.sh" && chmod +x embyonekey.sh && ./embyonekey.sh</code></pre><h2>

运行完毕
<br/>可以输入以下命令测试
```
nginx -t
```
查询是否报错
```
curl https://mb3admin.com/admin/service/registration/validateDevice
curl https://mb3admin.com/admin/service/registration/validateDevice/666
```
查看是否正确返回值



#### 客户端证书安装
如服务器正常白嫖后,客户端还是无法正确显示,一般是证书不正确,请在客户端安装证书
```
https://github.com/s1oz/embyonekey/blob/master/guomi.cer 
```
右键另存为文件名为guomi.cer的文件后安装相应设备上

Windows请安装才此目录下
<br/>![](https://github.com/s1oz/embyonekey/raw/master/window.png)

<br/>IOS需要安装后在设置--通用--关于手机--证书信任设置中把证书信任


## 感谢 时光轴 星辰 不会魔法的思思 教程引路
