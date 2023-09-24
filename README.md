# Halopipe-GFWlist (翻墙-科学上网-搭梯子)
> *你的邮箱有没有经常收到微软的安全提示邮件? 在你代理的出口地区尝试登陆你的系统? 游戏账号被盗? GPT为什么总是被拒或被封, 这些都是安全问题, 想要真正的全局代理吗? 想要真正隐藏自己的IP吗? 想要独享带宽畅玩游戏吗? 建立自己的安全专线吧, 一台轻量服务器一个命令就搞定.*
> #### 三方代理最大的问题是: 非常不安全, 非常不安全, 非常不安全, 重要的事情说三遍
> * 账号信息不受保护
> * 个人信息不受保护
> * 游戏数据不受保护
> 
> #### 自建代理的优势: 适合长期使用
> * 独享出口带宽
> * 真正的全局模式
> * 稳定的出口IP

#### 它是什么
* 它是一个代理服务, 提供点对点双向加密安全通信管道.
* 支持系统: macos-x64 | linux-x64 | win-x64.
* 它可稳定运行于局域网的某台设备上, 并为其他同网设备提供服务.

#### 如何搭建私有安全代理:
- 在GFW之外的任意地区有一台代理服务器. ([阿里云轻量应用服务器](https://www.aliyun.com/product/swas?spm=5176.28047174.J_4VYgf18xNlTAyFFbOuOQe.36.133d7e0eLPwR9q&scm=20140722.X_data-d4b68a29ba28f53e56fa._.V_1) 香港/新加坡 ¥24/月)
- 获取并部署 [Halopipe](https://halopipe.com/) 代理.
```
    // 初始化CA证书, AES密钥等
    $ .\bin\halopipe-win-x64.exe init
```
```
    // 更改配置
    "PROXY_HTTP": {
        "HTTP_GETWAY_PORT": 8888,
        "HTTP_GLOBAL_PORT": 8889,
            
        "HTTP_SERVER_PORT": 8886,
        "HTTP_SERVER_HOST": "x.x.x.x",
    }
    
    // 客户端
    $ .\bin\halopipe-win-x64.exe httpc

    // 服务端
    $ ./bin/halopipe-linux-x64 https
```
```
    // 后台启动后需回车确认, 否则会随终端结束而被杀掉.
    $ nohup ./bin/halopipe-linux-x64 https & echo $! > https.pid
    
    // 杀后台进程
    $ kill -9 `cat https.pid`
```




