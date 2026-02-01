
---
目录：[[AI 平台工具总览]]
上一页：
下一页：
关键词：
相关链接：

---

# ？？？Google oAuth（Redirect URL、Client ID、Client Secret）

> 注意：使用NAS的localhost或IP地址申请Google凭据的oAuth时会出错！因为安全原因，谷歌只接受localhost或域名，不接受IP！

https://www.youtube.com/watch?v=hLS5nwCoGeg

![image.png](https://repo.in4tree.com/2026/01/31_1769897372278.png)

![image.png](https://repo.in4tree.com/2026/01/31_1769897557452.png)


## NAS Docker中n8n实现Google认证

> 注意：NAS的localhost其实不是n8n的访问IP，所以NAS里的n8n不能用localhost！

![image.png](https://repo.in4tree.com/2026/01/31_1769896321564.png)


### 方法一：（localhost欺骗绕过伪装法，简单！）先在本地Docker创建n8n容器，正常去实现Google认证，再把秘钥和证书迁移至NAS

![image.png](https://repo.in4tree.com/2026/01/31_1769897592612.png)


### 方法二：使用Cloudflare网站购买的域名获取认证，Cloudflare通过隧道转发本地的n8n服务信息

1. 创建新的tunnel
![image.png](https://repo.in4tree.com/2026/01/31_1769897852417.png)

2. 配置Channel
![image.png](https://repo.in4tree.com/2026/01/31_1769897950199.png)

3. 复制Docker的运行命令和参数
![image.png](https://repo.in4tree.com/2026/01/31_1769898011263.png)

4. 本地用SSH服务去连接NAS，然后用上面的命令和参数重新启动运行docker

5. 在docker中安装n8n时，增加一个环境变量
![image.png](https://repo.in4tree.com/2026/01/31_1769898210943.png)

6. 本地通过域名访问NAS的n8n，完成注册登录和新建工作流
7. 添加Gmail并认证，可以看到这个回传地址就变成了我们输入的域名了
![image.png](https://repo.in4tree.com/2026/01/31_1769898355661.png)



# ？？？Notion

https://www.youtube.com/watch?v=qJodo176ao4


# ？？？Telegram


# ？？？飞书

