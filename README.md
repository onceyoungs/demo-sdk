### demo-sdk
>示例 SDK 开发并发布到composer仓库，仅供参考！

### 发布sdk到composer仓库
> 1、登录composer官网 https://packagist.org  
2、进入个人中心的设置页面连接github账号，绑定连接后发布的包会自动同步版本 https://packagist.org/profile/edit  
3、进入包提交页面 https://packagist.org/packages/submit  
4、把sdk的仓库地址填入后点击检查并提交  
5、审核通过后就能搜索到sdk了

### 发布sdk新版本并同步composer仓库
>1、将sdk要发布的分支打一个标签 `git tag -a v1.0.0 -m "v1.0.0"`  
2、提交标签到远程仓库 `git push origin v1.0.0`  
3、已配置composer绑定连接github账号的，发布新版本时会自动同步到composer仓库，否则需要手动同步