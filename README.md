# auto-telegram-bot-checkin
1. 利用github中的Action功能自动执行python脚本,自动给telegram中指定的机器人发送指定的命令
2. 温馨提示：Action要先执行一次激活才可以定时执行，由于Github的问题，执行并非准时，UTC时间不是北京时间，有8小时时差
3. https://crontab.guru/ 此网站可以编写Cron时间

## 使用步骤：
1. 首先在 https://my.telegram.org/ 中获取api和hash，并将代码中的信息替换为你自己的 API和hash
2. 先在本地跑通（下载整个项目，运行main.py），进行验证(输入手机号和验证码)，获取chat_name.session（自动生成在你的文件夹下），上传整个项目到github中。其中chat_name可以自定义名字
3. 首次使用需要将代码打包下载下来后输入手机号和验证码（code）获取账号相关session值自动保存在本地文件夹，记得加上手机区号，如+86
4. 根据需要调整代码。目前代码是向我指定的机器人发送一个/checkin指令，你可以改为你需要的机器人指令
5. 默认在UTC的4:01运行，北京时间00:01，可以自行修改
6. 在Actions中运行，验证是否部署成功
7. 请将仓库设置为private，确保你的私有密钥不会公开
8. 给本项目点个Star，支持下本项目
