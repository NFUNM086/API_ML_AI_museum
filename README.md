# 智能化博物馆（动静皆宜）
## 介绍
该产品是为多动症者/身障者提供观览博物馆的一个服务。
## MRD

随着社会快速发展，人们生活条件水平和经济能力不断提高，越来越多人会利用闲暇时间去参观博物馆。然而，特殊群体例如多动症者、身残者，他们无法获得参观博物馆的良好体验。

## BRD

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

**痛点一**（对应核心价值一）：多动症者无法控制自己的行为，可能会对博物馆的文物造成一定程度上的破坏，导致损失。

**痛点二**（对应核心价值二）：多动症者难以集中注意力参观博物馆，在人多的地方更是如此。

**痛点三**（对应核心价值三）：听力残障用户（假设他们不会唇语）无法通过讲解员的口述了解到该文物的介绍，用户体验极差。

### 需求列表与人工智能API加值 3%
| # | 目标用户 | 需求列表（痛点） | 场景 | 人工智能API | 优先级 | 备注 | 
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 多动症者 | 实时监测破坏文物的行为，避免不好的情况发生 | 多动症者无法控制自身行为，可能会对博物馆的文物造成破坏，导致损失 | 百度的危险行为 | 重要 | ff |
| 2 | 多动症者 | 通过动态人流量统计，推荐人流量较少区域为用户提供参考选择行程方案 | 多动症者无法集中注意力，在人流量较少的地方这种情况可能会一定程度上改善 | 百度的动态人流量统计 | 次重要 | ff |
| 3 | 耳残者 | 实时将讲解员的语音转换为可供阅读的文字 | 听力残障用户无法通过讲解员的口述了解到该文物的介绍 | 微软的语音识别 | 次重要 | ff |



### 人工智能概率性与用户痛点 3%
| # | 人工智能 | 可能出现的问题 | 概率性 | 用户痛点 | 评价 |
| --- | --- | --- | --- | --- | --- |
| 1 | 危险行为 | 可能由于视频分析等原因导致模糊行为的误判 | xx% | 导致对用户不必要的误解赫尔一定程度的伤害 | **问题较大**，用户体验大大降低 |
| 2 | 动态人流量统计 | 可能由于人物属性等问题导致识别结果不准确 | xx% | 识别结果不准确 | **问题不大** |
| 3 | 语音识别 | 可能由于语速、口音等问题导致识别结果不准确 | xx% | 不能准确理解讲说员表达的 | **问题不大**，用户体验可能会降低 |


### 原型

[原型链接](https://nfunm086.github.io/museum_prototype/)

#### 原型1.交互及界面设计
交互及界面设计：在PRD文件中是否有说明且原型是否有做到：交互及界面设计的某个核心交互环节使用了人工智能的加值

#### 原型2.信息设计
信息设计：在PRD文件中是否有说明且原型是否有做到：信息设计的某个核心信息或设计使用了人工智能的加值

#### 原型3.原型文档
原型文档：多少程度上有提供MVP可交互的原型文档，供它人在Github上下载使用

#### 原型4.口头操作说明
口头操作说明：多少程度上在2-3分钟时间限制内，对听众留下了「的确这是个可行丶可用的人工智能加值产品」的印象

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


#### 核心功能API三：语音识别（百度智能云）


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
- **接口描述**：统计图像中的人体个数和流动趋势，主要适用于低空俯拍、出入口场景，以人体头肩为主要识别目标
- **HTTP 方法**：POST
- **请求URL**：https://aip.baidubce.com/rest/2.0/image-classify/v1/body_tracking
- **评价**：镜子反射会导致识别错误



#### API3.使用后风险报告
使用后风险报告：在PRD文件中是否有说明且提供连结证据，所使用的API类别的现在及未来发展性，如API市场竞争程度丶输入输出限制丶定价丶及可替代的程序库（改用自己开发的代码及数据库而不用API）等等

#### API4.加分项
使用复杂度：用了2个以上机器学习与人工智能的API之输入及输出
