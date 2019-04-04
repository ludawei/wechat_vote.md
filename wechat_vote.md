# ###会员管理、问答模块
## 1.微信会员列表接口
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=QaApi&a=wxuserlist

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|page| String | 当前页数,不传则第一页
|nickname| String | 微信昵称搜索

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据   0:非GET请求
|headimgurl| String | 微信头像
|openid| String | 微信openid
|nickname| String | 微信昵称
|sex| String | 性别
|country| String | 国家
|province| String | 省份
|city| String | 城市
|score| String | 积分
|subscribe| String | 是否关注
|subscribe_time| String | 关注时间

## 2.广告列表接口
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=QaApi&a=advertisement

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据   0:非GET请求
|title| String | 广告标题
|topimg| String | 顶部广告小图
|topbigimg| String | 顶部广告大图
|midimg| String | 中部广告图
|bottomimg| String | 底部广告图
|etime| String | 生效开始时间
|btime| String | 生效结束时间


## 3.问答模块活动列表
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=QaApi&a=activity

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|id| String | 可根据id查详情

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据   0:非GET请求
|id| String | 唯一id
|name| String | 活动名称
|zhaiyao| String | 活动摘要
|logo| String | logo展示
|fx_logo| String | 分享logo
|fx_font| String | 分享文字
|zbdw| String | 主办单位

## 4.问答模块活动（添加/修改）
## 接口地址（POST）
http://zhejiang.welife100.com/system.php?m=QaApi&a=activity

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|id| String | 修改数据对应id,不传则添加
|name| String | 活动名称
|zhaiyao| String | 活动摘要
|info| String | 活动摘要
|logo| file| logo展示
|fx_logo| file| 分享logo
|fx_font| String | 分享文字
|zbdw| String | 主办单位

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败

## 5.问答模块活动删除
## 接口地址（get）
http://zhejiang.welife100.com/system.php?m=QaApi&a=activitydel

## 必传参数
字段名 | 类型 | 描述
|- | :-: | -:
|id| String | 删除数据的id

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败


## 6.问答模块问题列表
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=QaApi&a=questions

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|qid| String | 问题id，不传则查全部

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败
|name| String | 问题对应的活动名称
|qid| String | 问题id
|qtitle| String | 问题标题
|aqid| String | 活动id
|answer| String | 问题选项
|qtype| String | 问题类型
|tanswer| String | 答案

## 7.问答模块问题列表(添加/修改)
## 接口地址（POST）
http://zhejiang.welife100.com/system.php?m=QaApi&a=questions

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|qid| String | 问题id，不传则添加
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败
|name| String | 问题对应的活动名称
|qid| String | 问题id
|qtitle| String | 问题标题
|aqid| String | 活动id
|answer| String | 问题选项 例：["A","B","C","D"]
|qtype| String | 问题类型  1：单选  2：多选
|tanswer| String | 答案  例：["0","1","2","3"] 对应ABCD,如答案为A则["0"]
## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败


## 8.问答模块问题列表删除
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=QaApi&a=questionsdel

## 必选参数
字段名 | 类型 | 描述
|- | :-: | -:
|qid| String | 删除的问题id

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败

## 9.荣誉列表
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=QaApi&a=honor

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|jlid| String | 荣誉id,不传则查全部

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败
|name| String | 活动名称
|jl_id| String | 荣誉id
|jl_name| String | 荣誉名称
|aqid| String | 活动id
|jl_xuqiu| String | 荣誉所需分数
|jl_type| String | 荣誉类型
|jl_content| String | 荣誉内容

## 10.荣誉列表（添加/修改）
## 接口地址（POST）
http://zhejiang.welife100.com/system.php?m=QaApi&a=honor

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|jlid| String | 荣誉id,不传则添加
|name| String | 活动名称
|jl_id| String | 荣誉id
|jl_name| String | 荣誉名称
|aqid| String | 活动id
|jl_xuqiu| String | 荣誉所需分数
|jl_content| String | 荣誉内容
## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败

## 11.用户信息
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=QaApi&a=qauser

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|page| String | 页数
|wid| String | 活动id
## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败
|wdname| String | 活动名称
|level| String | 荣誉名称
|aqid| String | 活动id
|openid| String | 微信openid
|addtime| String | 添加时间
|fen| String | 用户得分
|nickname| String | 微信昵称
|headimgurl| String | 微信头像

# ###投票活动
## 1.投票活动列表
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=activity

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|id| String | id查详情

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据   0:非GET请求
|id| String | id自增
|name| String | 活动名称
|info| String | 活动信息
|logo| String | logo展示
|fx_logo| String | 分享logo
|fx_font| String | 分享内容
|tpprizenum| String | 每次抽奖需要票数
|piaonum| String | 个人每日票数
|zpiaonum| String | 个人总票数
|prizedaynum| String | 每日总奖品数量
|banner2| String | banner2
|banner1| String | banner1

## 2.投票活动（添加/修改）
## 接口地址（POST）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=activity

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|id| String | 传id修改，不传则添加
|name| String | 活动名称
|info| String | 活动信息
|logo| String | logo展示
|fx_logo| String | 分享logo
|fx_font| String | 分享内容
|tpprizenum| String | 每次抽奖需要票数
|piaonum| String | 个人每日票数
|zpiaonum| String | 个人总票数
|prizedaynum| String | 每日总奖品数量
|banner2| file| banner2
|banner1| file | banner1

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败

## 3.投票活动删除
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=activitydel

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|id| String | 删除数据的id


## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败

## 4.作品列表
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=works

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|aid| String | id查详情

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据
|name| String | 活动名称
|us_id| String | 作品id
|us_numset| String | 得票数
|us_oftoupiao| String | 所属活动id
|us_title| String | 作品名称
|us_content| String | 作品描述
|us_logo| String | 图片
|us_addtime| String | 添加时间
|us_media| String | 媒体资源

## 5.作品列表
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=works

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|aid| String | id查详情

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据
|name| String | 活动名称
|us_id| String | 作品id
|us_numset| String | 得票数
|us_oftoupiao| String | 所属活动id
|us_title| String | 作品名称
|us_content| String | 作品描述
|us_logo| String | 图片
|us_addtime| String | 添加时间
|us_media| String | 媒体资源


## 6.作品列表（添加/修改）
## 接口地址（POST）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=works

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|us_id| String | 修改的id，不传则添加
|name| String | 活动名称
|us_numset| String | 得票数
|us_oftoupiao| String | 所属活动id
|us_title| String | 作品名称
|us_content| String | 作品描述
|us_logo| file| 图片
|us_addtime| String | 添加时间
|us_media| file| 媒体资源

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据


## 7.作品列表删除
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=worksdel

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|us_id| String | 删除id

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   0：失败

## 8.奖品信息
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=prize


## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   404:空数据   0:非GET请求
|id| String | id自增
|name| String | 活动名称
|jll_id| String | 奖励id
|jll_name| String | 奖励标题
|jll_oftoupiao| String | 所属活动id
|jll_content| String | 奖励信息
|jll_logo| String | logo
|jll_maxcount| String | 奖品库存
|jll_isnull| String | 是否中奖 1是2否
|jll_jilv| String | 中奖概率
|jll_mes| String | 中奖提示信息

## 9.奖品信息（添加/修改）
## 接口地址（POST）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=prize

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|jll_id| String | 修改id,不传则添加
|jll_name| String | 奖励标题
|jll_oftoupiao| String | 所属活动id
|jll_content| String | 奖励信息
|jll_logo| String | logo
|jll_maxcount| String | 奖品库存
|jll_isnull| String | 是否中奖 1是2否
|jll_jilv| String | 中奖概率
|jll_mes| String | 中奖提示信息
## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败


## 10.奖品信息删除
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=prizedel

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|jll_id| String | 删除id

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功   0：失败


## 11.获奖列表
## 接口地址（GET）
http://zhejiang.welife100.com/system.php?m=VoteApi&a=winning

## 可选参数
字段名 | 类型 | 描述
|- | :-: | -:
|tpid| String | 投票id

## 返回值
字段名 | 类型 | 描述
|- | :-: | -:
|msg| String | 返回信息说明
|status| String | 状态码  200：成功  0:失败
|name| String | 活动名称
|nickname| String | 微信昵称
|headimgurl| String | 微信头像
|id| String | 状态码  获奖自增id
|uid| String | 状态码 微信openid
|jiangliid| String | 奖励id
|addtime| String | 添加时间
|toupiaoid| String | 投票id
