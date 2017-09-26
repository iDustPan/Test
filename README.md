## 别样面试小测试


- 你需要用到的API：

    `文章消息API：https://baleen-dev.bybieyang.com/feeds/comments?f=10&t=20`

    `晒单消息API：https://5thave-dev.bybieyang.com/api/v1/product-comment/feeds/comments?f=0&t=10`

- 参数含义：
    `f: 从第f条开始`
    `t: 取到第t条`
    比如f=10&t=20表示取第10~20条消息；

- Request Header:
``` 
  {
    "X-Session-Key" = "b85612b3-de4e-49ec-9238-ca8c0d3d6aab",
    "X-Session-User" = "48c85ab9-a7f5-4970-a310-f5c982fd9f4a"
  }
```


- API 说明：

** 注意 “replies”代表回复白色部分的内容，灰色部分的内容是最外层的(content)部分 **

```
{

"total": 1257,  //一共多少条数据

"from": 10, //从哪条开始取的

"to": 20, //取到哪条

"feeds":[{

        "id": "41912430-b198-4eb5-b251-4608a8a1b87f",

        "articleId": "dealhound_43655_945",

        "postedAt": 1503030125176, //评论时间戳

        "userLabel": "小北", //被回复的用户

        "userAvatar": "http://5thave-img-dev-cdn.bybieyang.com/img/hf/f1d5b69b-e879-4924-a50a-63b277126049", // 被回复用户的头像

        "content": "棒棒👍🏻",  // 评论内容

        "articleTitle": "更纤长、更浓密\n绽开黑天鹅羽扇", // 来自文章

        "replies": [

                    {
                    "id": "4b7184be-866e-4f6c-b55a-0e7bf0c7e68b",

                    "articleId": "dealhound_43655_945",

                    "postedAt": 1503030221029,  // 回复时间戳

                    "userLabel": "小北",

                    "userAvatar": "http://5thave-img-dev-cdn.bybieyang.com/img/hf/f1d5b69b-e879-4924-a50a-63b277126049",

                    "content": "要不要这么biang",   // 回复内容

                    }]  // 上面白色部分的回复信息
  }]

}  

  要求:
  
    1. 将两个API返回的数据合并，按回复的时间顺序分页展示“我的消息”；

    2. 实现分页功能，每页显示10条数据，上拉加载更多，下拉刷新，不仅单页的是按时间排序，页面与页面之前也是按时间排序的；

    3. 具体视觉效果看附件图片，有些细节如果不清楚可以自己定规则；

    4. 图片不需要点击展示高清大图；

    5. 上面的两个Tab“评论、客服”可做可不做，随意；
    
    6. 请不要直接在此直接提交代码；
    
    
    
    
    
    
    
    




