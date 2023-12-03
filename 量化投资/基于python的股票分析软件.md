基于Python的股票分析软件



最近，一位常年研究股票系统的[开发者](https://www.zhihu.com/search?q=开发者&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231}) pythonstock 用 Python 写了一个股票分析系统，发布数天就获得了不少关注。

于是我们就推荐给大家，既能学习 python 又能练习炒股。但正如项目作者所说，「本项目只能用于 Python 代码学习，股票分析，投资失败亏钱不负责，不算 BUG。」如果真亏了，我们也不背锅呀，毕竟大家都是韭菜。

![img](https://picx.zhimg.com/80/v2-7c940f463c2e2801c1ebb1f741d23b76_1440w.webp?source=1940ef5c)

*pythonstock 的项目页面*

总之，分析得准不准先不说，我们先来偷个师，看看这个用 Python 代码进行股票分析的项目到底是怎么实现的吧。

### **PythonStock：一个用 Python 写成的股票分析系统**

根据 GitHub 页面介绍，该项目是基于 Python 的 pandas、tushare、bokeh、tornado、stockstats、ta-lib 等框架开发的全栈股票系统。

**GitHub 地址**：https://github.com/pythonstock/stock

Gitee地址：https://gitee.com/pythonstock/stock

**它具备以下特点：**

1）可以直接使用 docker 本地部署运行，整个项目在 docker hub 上压缩后仅有 200BM，本地占用 500MB [磁盘空间](https://www.zhihu.com/search?q=磁盘空间&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})。

2）使用 Docker 解决 Python 库安装问题，使用 Mariadb（MySQL）[存储数据](https://www.zhihu.com/search?q=存储数据&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})，借助 tushare 抓取数据。

3）使用 corn 做[定时任务](https://www.zhihu.com/search?q=定时任务&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})，每天进行数据抓取计算，每天 18 点开始进行数据计算，计算当日数据，使用 300 天数据进行计算，大约需要 15 分钟计算完毕。

4）股票数据接口防止被封，按天进行数据缓存，储存最近 3 天数据，每天定时清除，同时使用 read_pickle to_pickle 的 gzip 压缩模式存储。

5）使用 tornado 开发 web 系统，支持股票数据、沪深 300 [成份股](https://www.zhihu.com/search?q=成份股&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})、中证 500 成份股、[龙虎榜数据](https://www.zhihu.com/search?q=龙虎榜数据&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})、[每日股票](https://www.zhihu.com/search?q=每日股票&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})数据、每日[大盘指数](https://www.zhihu.com/search?q=大盘指数&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})行情等。

6）数据展示系统：通用数据展示系统，配置字典模板之后，页面自动加载数据，并完成数据展示，后续可以加入自己开发的指标数据。

7）增加曲线数据分析：查看股票时，可以直接跳转到[东方财富](https://www.zhihu.com/search?q=东方财富&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})页面查看相关信息，点击指标之后使用 Bokeh 将多达 17 个指标的[数据可视化](https://www.zhihu.com/search?q=数据可视化&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})，进行图表展示。

![img](https://pic1.zhimg.com/80/v2-42e101ad8d557f6f2a86f871e942e793_1440w.webp?source=1940ef5c)

bokeh 绘图指标数据：

![img](https://picx.zhimg.com/80/v2-b400a906fe7955d48f0745162c249833_1440w.webp?source=1940ef5c)

然后根据 KDJ、RSI 和 CCI 这 3 个指标进行股票数据计算：

![img](https://picx.zhimg.com/80/v2-00d5226ffa99fefe5fddf8109d3593ae_1440w.webp?source=1940ef5c)

**[计算指标](https://www.zhihu.com/search?q=计算指标&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})**

此股票分析系统提供的每日股票指标数据，按照 17 个计算指标进行计算（下图截取部分计算指标）：

![img](https://picx.zhimg.com/80/v2-8694f34f22af45991f5851cde65460e7_1440w.webp?source=1940ef5c)

此外，项目作者还介绍了该股票[系统设计](https://www.zhihu.com/search?q=系统设计&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})原理、[架构设计](https://www.zhihu.com/search?q=架构设计&search_source=Entity&hybrid_search_source=Entity&hybrid_search_extra={"sourceType"%3A"answer"%2C"sourceId"%3A2925323231})原理、应用部署要点等知识，具体使用和部署方法参见 GitHub 项目页面。

![img](https://pic1.zhimg.com/80/v2-0fd8c036d1b796bc8bbe3c6f824a5841_1440w.webp?source=1940ef5c)

感兴趣的小伙伴，也许可以亲自上手试一试了。

不过，需要再次提醒的是，股市有风险，入市需谨慎哦。