# 智能化博物馆（动静皆宜）
## 介绍
该产品是为多动症者/身障者提供观览博物馆的一个服务。
## MRD

博物馆是一个国家文明和社会进步程度的标志，主要职能是在实现文物保护的基础上，通过展览展示、社会活动等形式，提高文物利用水平，起到文化传承的作用。
随着经济的发展和人们生活水平的不断提高，人们的文化素质逐步提高，精神文化需求也日益增长，参观博物馆成为人们生活中一个越来越重要的内容。

![我国博物馆数量.jpg](https://upload-images.jianshu.io/upload_images/9400767-98ac62d0b883a1db.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![我国博物馆参观人数（亿人次）.jpg](https://upload-images.jianshu.io/upload_images/9400767-8a7c12facb36aae4.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

尽管我国博物馆数量越来越多，但是从国际经验来看，我国博物馆建设方面的发展空间仍然是巨大的。**互联网作为当今时代最具发展活力的领域，已经全面融入生活的方方面面，博物馆依托互联网时代的技术与平台，开始重新焕发勃勃生机。**

## BRD

#### 商业价值

通过物联网重塑博物馆可以改变我们体验文物、艺术的方式，还可以激发未来博物馆的全新商业模式。而在未来，**智能化**能积极增强博物馆开展业务的方式，减少成本资源，增加游客体验，甚至可能增加其对社会的影响。
同样，随着社会发展和科技进步，博物馆正在不断地被重新重新定义。博物馆已不仅是收藏、保护、研究、展示文化遗产的机构，还成为服务人的全面发展、面向未来的文化服务和教育机构。
然而，一些特殊群体例如多动症者、身残者，他们无法获得参观博物馆的良好体验。**而该产品正是面对这样的特殊且小众群体，结合人工智能的技术，坚持以人为本，为他们提供关怀性服务，在为博物馆减轻成本、资源负担，带来良好收益的同时，也能有助于提升博物馆的社会形象。**

## PRD
## 价值主张设计
### 加值宣言
针对多动症者、身障者这两个特殊的小众人群，制定契合他们自身情况的智能化产品和服务，让该特殊群体都能享有观赏博物馆的权利，为该群体提供具有人文情怀的服务，提升博物馆的社会形象。

### 核心价值

**多动症者** 

1. 避免多动症者对博物馆文物进行破坏，该智能化产品会监控用户的行为。
2. 通过人体检测和追踪，进行动态人流量统计，推荐人流量比较少的区域给用户参考选择。

**身障者** 

3. 对于听力有残疾的人群，利用实时语音转文字的功能服务把讲解员的话语解说转换为文字，给予该类用户进行阅读。

### 用户痛点和场景

**痛点一**

多动症者无法控制自己的行为，可能会对博物馆的文物造成一定程度上的破坏，导致损失。

**痛点二**

多动症者难以集中注意力参观博物馆，在人多的地方这样情况的程度加深。

**痛点三**

听力残障用户（假设他们不会唇语）无法通过讲解员的口述了解到该文物的介绍，用户体验极差。

### 需求列表与人工智能API加值 3%
| 序号 | 目标用户 | 需求列表（痛点） | 场景 | 人工智能API | 优先级 |
| --- | --- | --- | --- | --- | --- |
| 1 | 多动症者 | 实时监测破坏文物的行为，避免不好的情况发生 | 多动症者无法控制自身行为，可能会对博物馆的文物造成破坏，导致损失 | 百度的危险行为 | 重要 |
| 2 | 多动症者 | 通过动态人流量统计，推荐人流量较少区域为用户提供参考选择行程方案 | 多动症者无法集中注意力，在人流量较少的地方这种情况可能会一定程度上改善 | 百度的动态人流量统计 | 次重要 |
| 3 | 耳残者 | 实时将讲解员的语音转换为可供阅读的文字 | 听力残障用户无法通过讲解员的口述了解到该文物的介绍 | 微软的语音识别 | 重要 |


### 人工智能概率性与用户痛点 3%
| # | 人工智能 | 可能出现的问题 | 概率性 | 用户痛点 | 评价 |
| --- | --- | --- | --- | --- | --- |
| 1 | 危险行为 | 可能由于视频分析等原因导致模糊行为的误判 | 90%以上 | 导致对用户不必要的误解赫尔一定程度的伤害 | **问题较大**，用户体验大大降低 |
| 2 | 动态人流量统计 | 可能由于人物属性等问题导致识别结果不准确 | 90%以上 | 识别结果不准确 | **问题不大** |
| 3 | 语音识别 | 可能由于语速、口音等问题导致识别结果不准确 | 90%以上 | 不能准确理解讲说员表达的 | **问题不大**，用户体验可能会降低 |

### 原型

**[原型链接](https://nfunm086.github.io/museum_prototype/)**

#### 交互及界面设计

![博物馆流程图1.png](https://upload-images.jianshu.io/upload_images/9400767-d8306349886d20f5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![博物馆流程图2.png](https://upload-images.jianshu.io/upload_images/9400767-bd04be58d8c18162.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

【若上图显示不出，可跳转至[页面](https://nfunm086.github.io/museum_prototype/#g=1&p=%E6%A0%B8%E5%BF%83%E5%8A%9F%E8%83%BD%E6%B5%81%E7%A8%8B%E5%9B%BE)进行查看，谢谢！】

#### 信息设计
##### ①“按住别松开”“松开即开始识别”“上滑取消”等信息提醒用户

![博物馆信息设计1.png](https://upload-images.jianshu.io/upload_images/9400767-b48e474a6e545f1d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![博物馆信息设计2.png](https://upload-images.jianshu.io/upload_images/9400767-38832d0c6ce0b6c5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

【若上图显示不出，可跳转至[页面1](https://nfunm086.github.io/museum_prototype/#g=1&p=%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%AB)和[页面2](https://nfunm086.github.io/museum_prototype/#g=1&p=%E8%AF%AD%E9%9F%B3%E8%AF%86%E5%88%AB%E4%B8%AD)进行查看，谢谢！】

##### ②“越大表示该区域人流量越多”用可视化图表体现人流量多的区域来提醒用户

![博物馆信息设计4.png](https://upload-images.jianshu.io/upload_images/9400767-7a851ba7a53e00ce.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
【若上图显示不出，可跳转至[页面](https://nfunm086.github.io/museum_prototype/#g=1&p=%E5%9C%BA%E6%99%AF%E8%B7%AF%E7%BA%BF%E6%8E%A8%E8%8D%90)进行查看，谢谢！】

#### 原型文档

[原型文档](https://nfunm086.github.io/museum_prototype/)

### API产品使用关键AI或机器学习之API的输出入展示
#### API1.使用水平
使用水平：在PRD文件中是否有说明且展示，核心功能所应用的API之输入及输出

#### 核心功能API一：人体检测-动态人流量统计（百度智能云）

**调用输入**

```
# encoding:utf-8
import requests
import base64

# client_id 为官网获取的AK， client_secret 为官网获取的SK
host = 'https://aip.baidubce.com/oauth/2.0/token?grant_type=client_credentials&client_id=【输入你的AK】&client_secret=【输入你的SK】'
response = requests.get(host)
if response:
    print(response.json())
# 得到access_token

request_url = "https://aip.baidubce.com/rest/2.0/image-classify/v1/body_num"
# 二进制方式打开图片文件
f = open('【图片路径】', 'rb')
img = base64.b64encode(f.read())

params = {"image":img}
access_token = '24.d1b826707988feca52ca6df8dd090ba1.2592000.1579846582.282335-18105519'
request_url = request_url + "?access_token=" + access_token
headers = {'content-type': 'application/x-www-form-urlencoded'}
response = requests.post(request_url, data=params, headers=headers)
if response:
    print (response.json())

```

**调出示例**

```
{'person_num': 6, 'log_id': 2179723181858567673}
```


#### 核心功能API二：语音识别（百度智能云）


**调用输入**
```
# coding=utf-8

import sys
import json
import base64
import time

IS_PY3 = sys.version_info.major == 3

if IS_PY3:
    from urllib.request import urlopen
    from urllib.request import Request
    from urllib.error import URLError
    from urllib.parse import urlencode
    timer = time.perf_counter
else:
    from urllib2 import urlopen
    from urllib2 import Request
    from urllib2 import URLError
    from urllib import urlencode
    if sys.platform == "win32":
        timer = time.clock
    else:
        # On most other platforms the best timer is time.time()
        timer = time.time

API_KEY = '你的API Key'
SECRET_KEY = '你的Secret Key'

# 需要识别的文件
AUDIO_FILE = './16k.pcm'  # 只支持 pcm/wav/amr 格式，极速版额外支持m4a 格式
# 文件格式
FORMAT = AUDIO_FILE[-3:]  # 文件后缀只支持 pcm/wav/amr 格式，极速版额外支持m4a 格式

CUID = '123456PYTHON'
# 采样率
RATE = 16000  # 固定值

# 普通版

DEV_PID = 1536  # 1537 表示识别普通话，使用输入法模型。1536表示识别普通话，使用搜索模型。根据文档填写PID，选择语言及识别模型
ASR_URL = 'http://vop.baidu.com/server_api'
SCOPE = 'audio_voice_assistant_get'  # 有此scope表示有asr能力，没有请在网页里勾选，非常旧的应用可能没有

#测试自训练平台需要打开以下信息， 自训练平台模型上线后，您会看见 第二步：“”获取专属模型参数pid:8001，modelid:1234”，按照这个信息获取 dev_pid=8001，lm_id=1234
# DEV_PID = 8001 ;   
# LM_ID = 1234 ;

# 极速版 打开注释的话请填写自己申请的appkey appSecret ，并在网页中开通极速版（开通后可能会收费）

# DEV_PID = 80001
# ASR_URL = 'http://vop.baidu.com/pro_api'
# SCOPE = 'brain_enhanced_asr'  # 有此scope表示有极速版能力，没有请在网页里开通极速版

# 忽略scope检查，非常旧的应用可能没有
# SCOPE = False

class DemoError(Exception):
    pass


"""  TOKEN start """

TOKEN_URL = 'http://openapi.baidu.com/oauth/2.0/token'


def fetch_token():
    params = {'grant_type': 'client_credentials',
              'client_id': API_KEY,
              'client_secret': SECRET_KEY}
    post_data = urlencode(params)
    if (IS_PY3):
        post_data = post_data.encode( 'utf-8')
    req = Request(TOKEN_URL, post_data)
    try:
        f = urlopen(req)
        result_str = f.read()
    except URLError as err:
        print('token http response http code : ' + str(err.code))
        result_str = err.read()
    if (IS_PY3):
        result_str =  result_str.decode()

    print(result_str)
    result = json.loads(result_str)
    print(result)
    if ('access_token' in result.keys() and 'scope' in result.keys()):
        print(SCOPE)
        if SCOPE and (not SCOPE in result['scope'].split(' ')):  # SCOPE = False 忽略检查
            raise DemoError('scope is not correct')
        print('SUCCESS WITH TOKEN: %s  EXPIRES IN SECONDS: %s' % (result['access_token'], result['expires_in']))
        return result['access_token']
    else:
        raise DemoError('MAYBE API_KEY or SECRET_KEY not correct: access_token or scope not found in token response')

"""  TOKEN end """

if __name__ == '__main__':
    token = fetch_token()

    speech_data = []
    with open(AUDIO_FILE, 'rb') as speech_file:
        speech_data = speech_file.read()

    length = len(speech_data)
    if length == 0:
        raise DemoError('file %s length read 0 bytes' % AUDIO_FILE)
    speech = base64.b64encode(speech_data)
    if (IS_PY3):
        speech = str(speech, 'utf-8')
    params = {'dev_pid': DEV_PID,
             #"lm_id" : LM_ID,    #测试自训练平台开启此项
              'format': FORMAT,
              'rate': RATE,
              'token': token,
              'cuid': CUID,
              'channel': 1,
              'speech': speech,
              'len': length
              }
    post_data = json.dumps(params, sort_keys=False)
    # print post_data
    req = Request(ASR_URL, post_data.encode('utf-8'))
    req.add_header('Content-Type', 'application/json')
    try:
        begin = timer()
        f = urlopen(req)
        result_str = f.read()
        print ("Request time cost %f" % (timer() - begin))
    except URLError as err:
        print('asr http response http code : ' + str(err.code))
        result_str = err.read()

    if (IS_PY3):
        result_str = str(result_str, 'utf-8')
    print(result_str)
    with open("result.txt","w") as of:
        of.write(result_str)
```

**输出示例**
```
{"corpus_no":"6774253558516847619","err_msg":"success.","err_no":0,"result":["北京科技馆"],"sn":"152492941491577253815"}
```

同时也会生成txt


#### API2.使用比较分析
使用比较分析：在PRD文件中是否有说明且提供连结证据，所使用的API是查找过最适用的（主要竞争者无或比较次），如考量其成熟度丶性价比丶等等
#### 动态人流量统计（百度智能云）
- **接口描述**：面向门店、通道等出入口场景，以头肩为识别目标，进行人体检测和追踪，根据目标轨迹判断进出区域方向，实现动态人数统计，返回区域进出人数。
- **HTTP 方法**：POST
- **请求URL**：https://aip.baidubce.com/rest/2.0/image-classify/v1/body_tracking
- **评价**：镜子反射会导致识别错误
- **优势**
1. 目前只能找到这一家**人流量统计**的api
2. ![百度人流量统计产品优势.png](https://upload-images.jianshu.io/upload_images/9400767-f9fcefd272fb86ed.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 语音识别（百度智能云）
- **HTTP 方法**：JSON/raw
- **TOKEN_URL**：http://openapi.baidu.com/oauth/2.0/token
- **评价**：比较准确
- **优势**
![百度语音识别优势.png](https://upload-images.jianshu.io/upload_images/9400767-546314bcad91f784.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


##### 一、API市场竞争程度
**1. 人流量统计**
目前只有百度智能云这一家做静态&动态的人流量统计api。
**2. 语音识别**
市场上不管是大公司（百度智能云、腾讯云、阿里云）还是专门做语音类的公司（讯飞、有道智云）都有相关的语音识别服务，这说明语音识别模块在如今市场上竞争激烈、需求量大。

##### 二、输入输出限制
**1. 人流量统计**
- 输入限制：分辨率建议720p以上，更低分辨率的图片也能识别，只是效果可能有差异。暂不适用夜间红外监控图片，后续会考虑扩展。
- 输出限制：

**2. 语音识别**
- 输入限制：录音文件时长不超过60s；只能支持普通话和略带口音的中文识别、支持粤语、四川话方言识别、支持英语识别。语音格式支持支持：pcm（不压缩）、wav（不压缩，pcm编码）、amr（压缩格式）、m4a（压缩格式，仅支持极速版模型，m4a格式输入适用于微信小程序的录音文件）。推荐pcm 采样率 ：16000 固定值。 编码：16bit 位深的单声道。


##### 三、定价
**1. 人流量统计**
[百度智能云]([https://ai.baidu.com/tech/body/num](https://ai.baidu.com/tech/body/num)
)
![百度智能云人流量统计产品定价.png](https://upload-images.jianshu.io/upload_images/9400767-ff9108dc5f64ce5e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**2. 语音识别**
[百度智能云]([https://ai.baidu.com/ai-doc/SPEECH/ck38lxnx8](https://ai.baidu.com/ai-doc/SPEECH/ck38lxnx8)
)
![百度语音识别产品价格.png](https://upload-images.jianshu.io/upload_images/9400767-6651b38c56e21885.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### API4.加分项
运用了2个人工智能api：语音识别api、动态人流量统计api

参考文献：
1. [2019年中国博物馆行业市场现状及发展趋势分析 国家鼓励政策推动行业进入文创时代](https://bg.qianzhan.com/report/detail/459/190523-18bae1f7.html);
2. [博物馆市场趋势](https://wenku.baidu.com/view/7576a920fe00bed5b9f3f90f76c66137ee064fb6.html)

