### demo-sdk
>示例 SDK 开发并发布到composer仓库，仅供参考！  

### 创建sdk
>1、在github新建一个公开的仓库  
2、使用git克隆仓库到本地  
3、手动或用命令初始化composer.json文件  
4、编写sdk代码  
5、把不需要发布的文件或目录如vendor等添加到.gitignore文件中  
6、提交代码到github仓库

### 通用sdk目录规范 按需使用
>demo-sdk         sdk开发目录  
├─bin             可执行文件目录  
├─config          配置文件目录  
├─docs            文档目录  
├─examples        示例代码目录  
├─resources       静态资源目录  
├─runtime         运行时目录放临时文件和缓存等  
├─src             功能实现目录  
│  ├─Api          功能   
│  ├─ ...         更多功能目录  
│  │  
│  └─helper.php   助手函数  
│  
├─tests           单元测试目录  
├─vendor          扩展类库目录  
├─.gitignore      忽略提交文件  
├─composer.json   composer定义文件  
├─LICENSE         开源授权说明文件  
├─README.md       sdk说明文件  
└─phpunit.xml     单元测试配置文件

### 发布sdk到composer仓库
> 1、登录composer官网 https://packagist.org  
2、进入个人中心的设置页面连接github账号，绑定连接后发布的包会自动同步版本 https://packagist.org/profile/edit  
3、进入包提交页面 https://packagist.org/packages/submit  
4、把sdk的仓库地址填入后点击检查并提交  
5、审核通过后就能搜索到sdk了

### 发布sdk新版本并同步到composer仓库
>1、将sdk要发布的分支打一个标签 `git tag -a v1.0.0 -m "v1.0.0"`  
2、提交标签到远程仓库 `git push origin v1.0.0`  
3、已配置composer绑定连接github账号的，发布新版本时会自动同步到composer仓库，否则需要手动同步

### 使用composer安装sdk
>1、第一种安装方式在项目根目录下执行 `composer require onceyoungs/demo-sdk`  
2、第二种安装方式在项目的composer.json文件中的require配置项里添加 `"onceyoungs/demo-sdk": "1.0.0"` 然后执行 `composer update`