#### 有道云笔记签到
签到领空间，登陆[有道云笔记](https://note.youdao.com/)使用cookie里的YNOTE_SESS签到，但过几天就会失效，所以也增加了用户名密码签到，然后更新YNOTE_SESS，密码使用了MD5加密。

将YNOTE_SESS,用户名,32位小写md5加密后的密码分别填入`data.json`中`noteyoudao`对应的字段。


#### 如何使用
> 本项目使用python3实现

1. 安装依赖
```
pip install requests 
```
2. 填写`data.json`，json里是登录所需要的一些账号信息。
3. 执行`python main.py`

#### 自动签到
Linux 自动签到参考[crontab](http://www.runoob.com/w3cnote/linux-crontab-tasks.html)

Windows 自动签到可以使用任务计划程序。

利用github actions自动签到，fork本仓库后开启actions，编辑.github/workflows/checkin.yml,在settings,Repository secrets里填写账号密码等在checkin里用到的信息后出发action动作就可以签到。

