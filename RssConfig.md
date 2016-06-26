一些大型的网站像 [开发者头条](http://feedmaker.kindle4rss.com/feeds/toutiao.io.xml) [mises.org](https://mises.org/feed/blog.rss) 
这类都基本提供了rss或者XML直接引用就行了。
而一些像微信公众号这样的，就很难获取到rss。
先说方法吧，用 feed43 来对爱微帮这类的内容抓取站生成rss。爱微帮的正则用这个 <div class="title">{*}title="{%}"{*}href="{%}"{*}{%}</div>
上面说的简略，不过Google之后都是很简单的。

接下来说为什么用这种方法，起初我试过 [wlwr/rss](https://github.com/wlwr/rss)但是抓取到RSS并不如我所愿，它储存为一个本地文件。
这是因为基于搜狐openid抓取的是从js中得到的，并不能将之直接转换为想要的rss格式。
后来，我试过微广场。但是内容也是存在js中的，kindleEar可以走HTML的300,301,302,303但是没有javascript引擎无法解析，
kindle上只会出现跳转中而没有内容。
这里必须先插一句，我所知的池，冯两位先生是不想被获取RSS的。不过github上只谈技术，有什么话可以到别地说。weibo Eren_Yeager

所以说如果你想要通过kindleear在kindle上看微信就只有用feed去烧录html的内容站了。
具体做法就不说了，说一下我完成之后出现的问题。
kindle上微信每一篇文章，都会在后面加上作者的名字和爱微帮。

<div class="title">
<a title="xxxxxxx" href="http://www.xxxx.com/yuedu/xx.html" target="_blank" >xxxx是xxx</a>
</div>

根据上面的正则，我觉得就是替换了 target="_blank" 把网站名称给加了进来。不过影响不大，可能别的站会好一点？
