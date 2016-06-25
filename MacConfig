感谢作者提供这么好用的工具，没钱捧钱场现在只能捧个人场了。
写一点Mac下的配置，以及登陆后台之后所必须进行的设置避免 wrong SRC_EMAIL 无法发送邮件的情形。

我当初配置的时候参考的是这个 http://gongm.in/2014/12/deploy-kindle-ear-on-mac/
最重要的有两点必须注意
1. config.py 修改 DOMAIN，把默认的 kindleear 改为你的 Application ID 不要动别的地方，比如把https改动了http，会导致失败。

2. 总结起来就是两行命令，Mac与windows的不同。
python /usr/local/bin/appcfg.py update app.yaml module-worker.yaml
python /usr/local/bin/appcfg.py update . 

执行完命令应该chrome自动就新开标签页进后台了。也可手动 http://你的 Application ID.appspot.com/setting 进去。
倒入XML/OPML或订阅，然后亚马逊设置里配置kindle信赖邮箱，你的gmail。
最后GAE Dashbord去setting你的email，介于GFW建议手动 
https://console.cloud.google.com/appengine/settings?project=你的 Application ID 点击修改，添加你刚刚设置的信赖gmail，保存。

大功告成，手动发送一次，应该就成功了。
