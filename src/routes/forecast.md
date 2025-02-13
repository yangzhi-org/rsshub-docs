# ❗️ Forecast and Alerts

## BADAN METEOROLOGI, KLIMATOLOGI, DAN GEOFISIKA(Indonesian) <Site url="bmkg.go.id"/>

### News <Site url="bmkg.go.id/" size="sm" />

<Route namespace="bmkg" :data='{"path":"/news","categories":["forecast"],"example":"/bmkg/news","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["bmkg.go.id/","bmkg.go.id/berita"]}],"name":"News","maintainers":["Shinanory"],"url":"bmkg.go.id/","location":"news.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### Recent Earthquakes <Site url="bmkg.go.id/" size="sm" />

<Route namespace="bmkg" :data='{"path":"/earthquake","categories":["forecast"],"example":"/bmkg/earthquake","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["bmkg.go.id/","bmkg.go.id/gempabumi-terkini.html"]}],"name":"Recent Earthquakes","maintainers":["Shinanory"],"url":"bmkg.go.id/","location":"earthquake.ts"}' :test='{"code":1,"message":"expected [ Array(1) ] to not include &#39;https://www.bmkg.go.id/gempabumi-terk…&#39;"}' />

## Outage.Report <Site url="outage.report"/>

### Report <Site url="outage.report" size="sm" />

<Route namespace="outagereport" :data='{"path":"/:name/:count?","categories":["forecast"],"example":"/outagereport/ubisoft/5","parameters":{"name":"Service name, spelling format must be consistent with URL","count":"Counting threshold, will only be written in RSS if the number of people who report to stop serving is not less than this number"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"Report","maintainers":["cxumol","nczitzk"],"description":"Please skip the local service area code for `name`, for example `https://outage.report/us/verizon-wireless` to `verizon-wireless`.","location":"index.ts"}' :test='{"code":1,"message":"expected 503 to be 200 // Object.is equality"}' />

Please skip the local service area code for `name`, for example `https://outage.report/us/verizon-wireless` to `verizon-wireless`.

## Uptime Robot <Site url="rss.uptimerobot.com"/>

### RSS <Site url="rss.uptimerobot.com" size="sm" />

<Route namespace="uptimerobot" :data='{"path":"/rss/:id/:routeParams?","categories":["forecast"],"example":"/uptimerobot/rss/u358785-e4323652448755805d668f1a66506f2f","parameters":{"id":"the last part of your RSS URL (e.g. `u358785-e4323652448755805d668f1a66506f2f` for `https://rss.uptimerobot.com/u358785-e4323652448755805d668f1a66506f2f`)","routeParams":"extra parameters, see the table below"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["rss.uptimerobot.com/:id"],"target":"/rss/:id"}],"name":"RSS","maintainers":["Rongronggg9"],"description":"| Key    | Description                                                              | Accepts        | Defaults to |\n  | ------ | ------------------------------------------------------------------------ | -------------- | ----------- |\n  | showID | Show monitor ID (disabling it will also disable link for each RSS entry) | 0/1/true/false | true        |","location":"rss.ts"}' :test='{"code":0}' />

| Key    | Description                                                              | Accepts        | Defaults to |
  | ------ | ------------------------------------------------------------------------ | -------------- | ----------- |
  | showID | Show monitor ID (disabling it will also disable link for each RSS entry) | 0/1/true/false | true        |

## 地震速报 <Site url="www.ceic.ac.cn"/>

### 中国地震台 <Site url="www.cea.gov.cn/cea/xwzx/zqsd/index.html" size="sm" />

<Route namespace="earthquake" :data='{"path":"/ceic/:type?","categories":["forecast"],"example":"/earthquake/ceic/1","parameters":{"type":"类型，见下表"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["www.cea.gov.cn/cea/xwzx/zqsd/index.html","www.cea.gov.cn/"],"target":""}],"name":"中国地震台","maintainers":["SettingDust"],"url":"www.cea.gov.cn/cea/xwzx/zqsd/index.html","description":"| 参数 | 类型                        |\n  | ---- | --------------------------- |\n  | 1    | 最近 24 小时地震信息        |\n  | 2    | 最近 48 小时地震信息        |\n  | 5    | 最近一年 3.0 级以上地震信息 |\n  | 7    | 最近一年 3.0 级以下地震     |\n  | 8    | 最近一年 4.0 级以上地震信息 |\n  | 9    | 最近一年 5.0 级以上地震信息 |\n  | 0    | 最近一年 6.0 级以上地震信息 |\n\n  可通过全局过滤参数订阅您感兴趣的地区.","location":"ceic.ts"}' :test='{"code":1,"message":"expected 503 to be 200 // Object.is equality"}' />

| 参数 | 类型                        |
  | ---- | --------------------------- |
  | 1    | 最近 24 小时地震信息        |
  | 2    | 最近 48 小时地震信息        |
  | 5    | 最近一年 3.0 级以上地震信息 |
  | 7    | 最近一年 3.0 级以下地震     |
  | 8    | 最近一年 4.0 级以上地震信息 |
  | 9    | 最近一年 5.0 级以上地震信息 |
  | 0    | 最近一年 6.0 级以上地震信息 |

  可通过全局过滤参数订阅您感兴趣的地区.

### 中国地震局 <Site url="www.cea.gov.cn/cea/xwzx/zqsd/index.html" size="sm" />

<Route namespace="earthquake" :data='{"path":"/:region?","categories":["forecast"],"example":"/earthquake","parameters":{"region":"区域，0全部，1国内（默认），2国外"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":true,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["www.cea.gov.cn/cea/xwzx/zqsd/index.html","www.cea.gov.cn/"],"target":""}],"name":"中国地震局","maintainers":["LogicJake"],"url":"www.cea.gov.cn/cea/xwzx/zqsd/index.html","description":"可通过全局过滤参数订阅您感兴趣的地区.","location":"index.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

可通过全局过滤参数订阅您感兴趣的地区.

## 和风天气 <Site url="qweather.com"/>

### 近三天天气 <Site url="qweather.com" size="sm" />

<Route namespace="qweather" :data='{"path":"/3days/:location","categories":["forecast"],"example":"/qweather/3days/广州","parameters":{"location":"N"},"features":{"requireConfig":[{"name":"HEFENG_KEY","description":""}],"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"近三天天气","maintainers":["Rein-Ou","la3rence"],"description":"需自行注册获取 api 的 key，并在环境变量 HEFENG_KEY 中进行配置，获取订阅近三天天气预报","location":"3days.ts"}' :test='undefined' />

需自行注册获取 api 的 key，并在环境变量 HEFENG_KEY 中进行配置，获取订阅近三天天气预报

### 实时天气 <Site url="qweather.com" size="sm" />

<Route namespace="qweather" :data='{"path":"/now/:location","categories":["forecast"],"example":"/qweather/广州","parameters":{"location":"N"},"features":{"requireConfig":[{"name":"HEFENG_KEY","description":""}],"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"实时天气","maintainers":["Rein-Ou"],"description":"需自行注册获取 api 的 key，每小时更新一次数据","location":"now.ts"}' :test='undefined' />

需自行注册获取 api 的 key，每小时更新一次数据

## 停水通知 <Site url="swj.dl.gov.cn"/>

配合 [IFTTT](https://ifttt.com/) Applets [邮件通知](https://ifttt.com/applets/SEvmDVKY-) 使用实现自动通知效果.

### Unknown <Site url="whwater.com/IWater.shtml" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/wuhan/:channelId?","radar":[{"source":["whwater.com/IWater.shtml","whwater.com/"],"target":"/wuhan"}],"name":"Unknown","maintainers":[],"url":"whwater.com/IWater.shtml","location":"wuhan.ts"}' :test='undefined' />

### 大连市 <Site url="swj.dl.gov.cn/col/col4296/index.html" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/dalian","categories":["forecast"],"example":"/tingshuitz/dalian","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["swj.dl.gov.cn/col/col4296/index.html","swj.dl.gov.cn/"]}],"name":"大连市","maintainers":["DIYgod"],"url":"swj.dl.gov.cn/col/col4296/index.html","location":"dalian.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 东莞市 <Site url="swj.dl.gov.cn" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/dongguan","categories":["forecast"],"example":"/tingshuitz/dongguan","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"东莞市","maintainers":["victoriqueko"],"location":"dongguan.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 广州市 <Site url="swj.dl.gov.cn" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/guangzhou","categories":["forecast"],"example":"/tingshuitz/guangzhou","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"广州市","maintainers":["xyqfer"],"location":"guangzhou.ts"}' :test='{"code":0}' />

### 杭州市 <Site url="www.hzwgc.com/public/stop_the_water" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/hangzhou","categories":["forecast"],"example":"/tingshuitz/hangzhou","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["www.hzwgc.com/public/stop_the_water","www.hzwgc.com/"]}],"name":"杭州市","maintainers":["znhocn"],"url":"www.hzwgc.com/public/stop_the_water","location":"hangzhou.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 南京市 <Site url="jlwater.com/portal/10000013" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/nanjing","categories":["forecast"],"example":"/tingshuitz/nanjing","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["jlwater.com/portal/10000013","jlwater.com/"]}],"name":"南京市","maintainers":["ocleo1"],"url":"jlwater.com/portal/10000013","location":"nanjing.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 深圳市 <Site url="sz-water.com.cn/*" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/shenzhen","categories":["forecast"],"example":"/tingshuitz/shenzhen","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["sz-water.com.cn/*"]}],"name":"深圳市","maintainers":["lilPiper"],"url":"sz-water.com.cn/*","description":"可能仅限中国大陆服务器访问，以实际情况为准。","location":"shenzhen.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

可能仅限中国大陆服务器访问，以实际情况为准。

### 西安市 <Site url="swj.dl.gov.cn" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/xian","categories":["forecast"],"example":"/tingshuitz/xian","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"西安市","maintainers":["ciaranchen"],"location":"xian.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 萧山区 <Site url="www.xswater.com/gongshui/channels/227.html" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/xiaoshan","categories":["forecast"],"example":"/tingshuitz/xiaoshan","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["www.xswater.com/gongshui/channels/227.html","www.xswater.com/"]}],"name":"萧山区","maintainers":["znhocn"],"url":"www.xswater.com/gongshui/channels/227.html","location":"xiaoshan.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 阳江市 <Site url="yjsswjt.com/zxdt_list.jsp" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/yangjiang","categories":["forecast"],"example":"/tingshuitz/yangjiang","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["yjsswjt.com/zxdt_list.jsp","yjsswjt.com/"]}],"name":"阳江市","maintainers":["ciaranchen"],"url":"yjsswjt.com/zxdt_list.jsp","location":"yangjiang.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 长沙市 <Site url="swj.dl.gov.cn" size="sm" />

<Route namespace="tingshuitz" :data='{"path":"/changsha/:channelId?","categories":["forecast"],"example":"/tingshuitz/changsha/78","parameters":{"channelId":"N"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"长沙市","maintainers":["shansing"],"description":"可能仅限于中国大陆服务器访问，以实际情况为准。\n\n  | channelId | 分类     |\n  | --------- | -------- |\n  | 78        | 计划停水 |\n  | 157       | 抢修停水 |","location":"changsha.ts"}' :test='{"code":0}' />

可能仅限于中国大陆服务器访问，以实际情况为准。

  | channelId | 分类     |
  | --------- | -------- |
  | 78        | 计划停水 |
  | 157       | 抢修停水 |

## 中国气象局 <Site url="weather.cma.cn"/>

### 天气预报频道 <Site url="weather.cma.cn" size="sm" />

<Route namespace="cma" :data='{"path":"/channel/:id?","categories":["forecast"],"example":"/cma/channel/380","parameters":{"id":"分类，见下表，可在对应频道页 URL 中找到，默认为 380，即每日天气提示"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"name":"天气预报频道","maintainers":["nczitzk"],"description":"#### 天气实况\n\n  | 频道名称 | 频道 id                          |\n  | -------- | -------------------------------- |\n  | 卫星云图 | d3236549863e453aab0ccc4027105bad |\n  | 单站雷达 | 103                              |\n  | 降水量   | 18                               |\n  | 气温     | 32                               |\n  | 土壤水分 | 45                               |\n\n  #### 气象公报\n\n  | 频道名称       | 频道 id                          |\n  | -------------- | -------------------------------- |\n  | 每日天气提示   | 380                              |\n  | 重要天气提示   | da5d55817ad5430fb9796a0780178533 |\n  | 天气公报       | 3780                             |\n  | 强对流天气预报 | 383                              |\n  | 交通气象预报   | 423                              |\n  | 森林火险预报   | 424                              |\n  | 海洋天气公报   | 452                              |\n  | 环境气象公报   | 467                              |\n\n  :::tip\n  订阅更多细分频道，请前往对应上级频道页，使用下拉菜单选择项目后跳转到目标频道页，查看其 URL 找到对应频道 id\n  :::","location":"channel.ts"}' :test='{"code":0}' />

#### 天气实况

  | 频道名称 | 频道 id                          |
  | -------- | -------------------------------- |
  | 卫星云图 | d3236549863e453aab0ccc4027105bad |
  | 单站雷达 | 103                              |
  | 降水量   | 18                               |
  | 气温     | 32                               |
  | 土壤水分 | 45                               |

  #### 气象公报

  | 频道名称       | 频道 id                          |
  | -------------- | -------------------------------- |
  | 每日天气提示   | 380                              |
  | 重要天气提示   | da5d55817ad5430fb9796a0780178533 |
  | 天气公报       | 3780                             |
  | 强对流天气预报 | 383                              |
  | 交通气象预报   | 423                              |
  | 森林火险预报   | 424                              |
  | 海洋天气公报   | 452                              |
  | 环境气象公报   | 467                              |

  :::tip
  订阅更多细分频道，请前往对应上级频道页，使用下拉菜单选择项目后跳转到目标频道页，查看其 URL 找到对应频道 id
  :::

## 中国国家应急广播 <Site url="cneb.gov.cn"/>

### Unknown <Site url="cneb.gov.cn/yjxx" size="sm" />

<Route namespace="cneb" :data='{"path":"/yjxx/*","radar":[{"source":["cneb.gov.cn/yjxx","cneb.gov.cn/"],"target":"/yjxx"}],"name":"Unknown","maintainers":[],"url":"cneb.gov.cn/yjxx","location":"yjxx.ts"}' :test='undefined' />

### 应急新闻 <Site url="cneb.gov.cn" size="sm" />

<Route namespace="cneb" :data='{"path":"/yjxw/:category?","categories":["forecast"],"example":"/cneb/yjxw","parameters":{"category":"分类，见下表，默认为全部"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["cneb.gov.cn/yjxw/:category?","cneb.gov.cn/"]}],"name":"应急新闻","maintainers":["nczitzk"],"description":"| 全部 | 国内新闻 | 国际新闻 |\n  | ---- | -------- | -------- |\n  |      | gnxw     | gjxw     |","location":"yjxw.ts"}' :test='{"code":0}' />

| 全部 | 国内新闻 | 国际新闻 |
  | ---- | -------- | -------- |
  |      | gnxw     | gjxw     |

## 中国人民银行 <Site url="kjt.ah.gov.cn"/>

<details>
  <summary>*业务咨询* 和 *投诉建议* 可用的站点参数</summary>

  | 上海市   | 北京市  | 天津市  | 河北省 |
  | -------- | ------- | ------- | ------ |
  | shanghai | beijing | tianjin | hebei  |

  | 山西省 | 内蒙古自治区 | 辽宁省   | 吉林省 |
  | ------ | ------------ | -------- | ------ |
  | shanxi | neimenggu    | liaoning | jilin  |

  | 黑龙江省     | 江苏省  | 浙江省   | 安徽省 |
  | ------------ | ------- | -------- | ------ |
  | heilongjiang | jiangsu | zhejiang | anhui  |

  | 福建省 | 江西省  | 山东省   | 河南省 |
  | ------ | ------- | -------- | ------ |
  | fujian | jiangxi | shandong | henan  |

  | 湖北省 | 湖南省 | 广东省    | 广西壮族自治区 |
  | ------ | ------ | --------- | -------------- |
  | hubei  | hunan  | guangdong | guangxi        |

  | 海南省 | 重庆市    | 四川省  | 贵州省  |
  | ------ | --------- | ------- | ------- |
  | hainan | chongqing | sichuan | guizhou |

  | 云南省 | 西藏自治区 | 陕西省  | 甘肃省 |
  | ------ | ---------- | ------- | ------ |
  | yunnan | xizang     | shaanxi | gansu  |

  | 青海省  | 宁夏回族自治区 | 新疆维吾尔自治区 | 大连市 |
  | ------- | -------------- | ---------------- | ------ |
  | qinghai | ningxia        | xinjiang         | dalian |

  | 宁波市 | 厦门市 | 青岛市  | 深圳市   |
  | ------ | ------ | ------- | -------- |
  | ningbo | xiamen | qingdao | shenzhen |
</details>

### 广东省内城市预警信号 <Site url="www.tqyb.com.cn/gz/weatherAlarm/otherCity/" size="sm" />

<Route namespace="gov" :data='{"path":"/guangdong/tqyb/sncsyjxh","categories":["forecast"],"example":"/gov/guangdong/tqyb/sncsyjxh","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["www.tqyb.com.cn/gz/weatherAlarm/otherCity/"]}],"name":"广东省内城市预警信号","maintainers":["Fatpandac"],"url":"www.tqyb.com.cn/gz/weatherAlarm/otherCity/","location":"guangdong/tqyb/sncsyjxh.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

### 突发性天气提示 <Site url="www.tqyb.com.cn/gz/weatherAlarm/suddenWeather/" size="sm" />

<Route namespace="gov" :data='{"path":"/guangdong/tqyb/tfxtq","categories":["forecast"],"example":"/gov/guangdong/tqyb/tfxtq","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["www.tqyb.com.cn/gz/weatherAlarm/suddenWeather/"]}],"name":"突发性天气提示","maintainers":["Fatpandac"],"url":"www.tqyb.com.cn/gz/weatherAlarm/suddenWeather/","location":"guangdong/tqyb/tfxtq.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

## 中央气象台 <Site url="nmc.cn"/>

### 全国气象预警 <Site url="nmc.cn/publish/alarm.html" size="sm" />

<Route namespace="nmc" :data='{"path":"/weatheralarm/:province?","categories":["forecast"],"example":"/nmc/weatheralarm/广东省","parameters":{"province":"省份"},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["nmc.cn/publish/alarm.html","nmc.cn/"],"target":"/weatheralarm"}],"name":"全国气象预警","maintainers":["ylc395"],"url":"nmc.cn/publish/alarm.html","location":"weatheralarm.ts"}' :test='{"code":0}' />

## 重庆燃气 <Site url="cqgas.cn"/>

### 停气检修通知 <Site url="cqgas.cn/" size="sm" />

<Route namespace="cqgas" :data='{"path":"/tqtz","categories":["forecast"],"example":"/cqgas/tqtz","parameters":{},"features":{"requireConfig":false,"requirePuppeteer":false,"antiCrawler":false,"supportBT":false,"supportPodcast":false,"supportScihub":false},"radar":[{"source":["cqgas.cn/"]}],"name":"停气检修通知","maintainers":["Mai19930513"],"url":"cqgas.cn/","location":"tqtz.ts"}' :test='{"code":1,"message":"Test timed out in 10000ms.\nIf this is a long-running test, pass a timeout value as the last argument or configure it globally with \"testTimeout\"."}' />

