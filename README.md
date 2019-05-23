# YoudaoTranslate
破解有道翻译(最新加密破解)
请求头必须带上cookie,user-agent,refer 三者缺一不可
有道翻译接口数据加密字段有三个
ts ,salt,sign
其他字段可按照抓包返回的数据填入固定值
浏览器断点调试可知
ts字段时间戳，单位为毫秒

salt字段为ts加上一个1到10之间的随机数组成的字符串、

sign字段为"fanyideskweb" + 待翻译字符串 + salt + "@6f#X3=cCuncYssPsuRUE"

直接在本地运行python代码生成上述字段 向接口发送post请求即可
