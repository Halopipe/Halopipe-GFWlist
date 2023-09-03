# halopipe-gfwlist
*翻墙-科学上网-搭梯子, 简单小巧的自建安全代理工具.*

#### 免费的和非独享的最大的问题是: 
# 非常不安全, 非常不安全, 非常不安全, 重要的事情说三遍, 各方面都非常不安全.

#### 自建代理的优势:
- 独享出口带宽
- 私有加密绝对安全
- 真全局代理模式
- 静态IP安全稳定
- 长期使用性价比高

#### 如何搭建私有安全代理:
- 你得有一台代理服务器, 可以在境外任何地方. ([阿里云轻量应用服务器](https://www.aliyun.com/product/swas?spm=5176.28047174.J_4VYgf18xNlTAyFFbOuOQe.36.133d7e0eLPwR9q&scm=20140722.X_data-d4b68a29ba28f53e56fa._.V_1) 香港/新加坡 ¥24/月)
- 可运行于局域网内的任何一台设备, 并对局域网内其他设备提供代理服务.
- 提供双向加密, 不必担心数据在传输过程中被窥视.
- 获取并安装 [Halopipe](https://halopipe.com/) 代理.
  1. 初始化
    ```
      $ ./halopipe-macos-x64 init
    ```
  2. 配置端口号和服务器地址(服务端端口需要允许外部访问, 在防火墙或者云管理中开启.)
    ```
      "PROXY_HTTP": {
          "HTTP_GETWAY_PORT": 8888,
          "HTTP_GLOBAL_PORT": 8889,
            
          "HTTP_SERVER_PORT": 8886,
          "HTTP_SERVER_HOST": "x.x.x.x",
      }
    ```
  3. 下载并覆盖 [domainlist.json](https://github.com/Halopipe/halopipe-gfwlist/blob/main/domainlist.json)
  4. 启动本地和服务端代理程序
    ```
      // 客户端
      $ ./halopipe-macos-x64 httpc

      // 服务端
      $ ./halopipe-linux-x64 https
    ```
  5. 配置系统代理, 参考完整文档 [Halopipe](https://halopipe.com/)




