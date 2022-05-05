# nonebot-plugin-covid19-news 😷
国内新冠消息查询

## 安装使用
### 方法一 使用nb-cli
```
nb plugin install nonebot_plugin_covid19_news
```

### 方法二 使用pip
```
# pip 下载包
pip install nonebot_plugin_covid19_news


# 配置 pyproject.toml

plugins = [
    ...,
    "nonebot_plugin_covid19_news",
    ]

```


## 指令列表

### 查询地方疫情信息（风险等级 新增 目前确诊） 
指令: `城市名 + 疫情`  
事例: `天津疫情` 


### 查询地方出入政策  
指令: `城市名 + 疫情政策`  
事例: `广州疫情政策`

### 查询城市风险地区
*只限查询大陆地级市或直辖市*  
指令: `城市名 + 风险地区` 


###  疫情信息更新推送 
指令: `关注疫情 + 城市名`  
事例: `关注疫情 北京`

### 取消推送
指令: `取消疫情 + 城市名` / `取消关注疫情 + 城市名` / `取消推送疫情 + 城市名`

## 其他功能

### 异常新增警告
对国内新增异常的地区进行推送提醒  
需要修改配置文件`.env.dev`
```
COVID19 = {"notice":"True", "red-line": 1000, "filter":[],"group":[]}

// 字段说明
// notice: str              仅为 True 时开启功能
// red-line: int            新增达到该数值会, 发送疫情信息
// filter: List             过滤城市/地区 （默认过滤 香港 台湾）
// group: List[int] | str   发送到群; 为 all 时发送到所有群

```


## 更新log 📝
### 2022.2.14
添加取消推送功能

### 2022.2.15
添加风险地区查询功能功能

### 2022.3.23
无症状与确诊分开显示数据

### 2022.3.28
添加地区新增异常警告功能

### 2022.4.14
优化更新数据与推送的逻辑

## 注意⚠️
数据更新、消息推送 目前以30分钟为周期  
本插件使用腾讯api, 在疫情发生地(频繁大规模核酸) 数据存在一定滞后性, 真实数据请以国家公布为准
## 后续可能添加的功能
- [x] 定时推送关注城市疫情信息 ⏰
- [ ] 一周内疫情变化图表 📈

- 有想法欢迎提 issue 💡

