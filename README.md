# 优化不易，我用python
## page.py

一个链接：http://www.vrnew.com/index.php/News/newscontent/id/612
1. 它的title
2. 它的keywords
3. 它的description
4. 它的模拟抓取内容结果
5. 它是否被baidu收录
6. 它是否被so收录
7. 它是否被sogou收录
8. 它的内链有哪些 共多少条
9. 它的外链有哪些 共多少条
10. 它有哪些些词汇呢？举例：{url:"http://www.vrnew.com/index.php/News/newscontent/id/612 " ,wordlist=[("首页",433),("vr",23),("Vr公司",20),("华锐视点",10),("北京虚拟现实",10),("虚拟现实公司",10),("北京华锐视点_VR虚拟现实/AR增强现实内容制作公司",1)]}

## word.py

# word.py简介
``` python
> import word
> word.baidu_index("seo",0)
>  [{'data-click': None,
  'domain': 'baike.baidu.com/',
  'id': '1',
  'srcid': '91',
  'title': 'SEO_百度百科',
  'tpl': 'bk_polysemy'},.....]
>  word.get_index_baidu("www.vrnew.com",*["华锐视点","vr","虚拟现实"])
>  [{'rank': ['1', '66', '93'], 'word': '华锐视点'},
 {'rank': ['86'], 'word': 'vr'},
 {'rank': ['48'], 'word': '虚拟现实'}]
```

seoer最基本的就是挖词，这些词怎么来？
1. 几家搜索引擎搜索结果相关搜索、SUG
2. 几家大的社交、媒体（微博）的相关搜索
3. 各搜索引擎的风云榜
4. 竞价关键词获取工具（搜索引擎一般都提供）
5. 百度司南工具
6. Log日志关键词数据
7. 站内搜索关键词数据
8. 商务通、商桥等在线咨询工具内的关键词
9. 竞争对手网站上的tag页
10. 竞争对手（尤其是对seo很重视的）站点title
11. 竞争对手竞价关键词
12. 竞争对手页面keyword
13. cnzz数据

***
|-vr   
|-vr->眼镜 	  
|-vr->眼镜->原理   
|-vr->眼镜->排行     
|-vr->眼镜->是\什么		    
|-vr->眼镜->怎么\用/怎么\使用                                   	      
|-vr->眼镜->多少\钱		   
|-vr->眼镜->哪个\牌子\好    
|-vr->眼镜->看\片\什么\感觉    
|-vr->眼镜->看\的\毛片\哪里有             
|-vr->眼镜->几十元\的\有\效果\吗                      
|-vr->眼镜->能看\普通\岛国\片                  
|-vr->眼镜->怎么\链接\电脑                                        
|-vr->眼镜->视频\资源\岛国       

### 关键词排名定位 

baidu_index("外卖")
返回结果
![](https://github.com/haizhilong/chinaseotools/blob/master/screenshot/TIM%E6%88%AA%E5%9B%BE20170606112641.png)

## site.py
在这个包里，想实现对服务器数据的抽取，以及网站相关信息的调查，还有一些数据的统计分析                       
目前有：                                   
1. whois信息的抽取                         
2. domain->ip    
3. 服务器环境
4. robots文件的抽取
5. 站点内所有的连接
6. baidu收录数统计 以及已经收录的连接
7. so收录数据统计 以及已经收录的连接
8. sogou收录数据统计 以及以及收录的连接
一些功能：    
1. 生成网站地图
2. 生成死链文档
3. 友情链接检测
4. 网站日志分析（限于iis日志，apache日志暂不能处理）

