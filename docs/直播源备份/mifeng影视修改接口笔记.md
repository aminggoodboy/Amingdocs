# 接口

看到别人修改了接口十分好奇是怎么找到的

后来分析发现自己能力不足，只能分析别人找到的代码

最终发现特征

1. MT管理器dex搜索【“name”】然后在结果内搜索【config_】，就可以找到该界面
2. 发现直接搜索【config_】更快，更方便找到位置



下面是示例，就在这些代码附近

![Wf57rLY9Pj.png](https://picshack.net/ib/Wf57rLY9Pj.png)

![b2Y3orqC4e.png](https://picshack.net/ib/b2Y3orqC4e.png)

# 设置里面版本号 改为自定义

搜索 Missing required view with ID: 

再搜索2.2.3或其他版本号

修改成你想要的文字内容

# 去更新

搜索leanback.json或者mobile.json

进去直接把这个名字删掉，就好了