#an-card 卡片
使用[ColorUI](https://www.color-ui.com/)封装的卡片组件，组件名:`NAUI-card`,代码块: `NAUIcard`。
ColorUI是一款出色的纯css组件库，可以与任何组件结合，大大加快开发效率!

更新说明：

增加卡片内容属性-`listData.creat_time`(帖子创建时间)，数据类型可为number或string。注意如果非unix时间戳需要将组件生命周期中调用时的*1000删掉。默认为unix时间戳，已做处理。

## 使用方式

在需要使用的页面中引入:

```
import NAUIcard from '@/components/NAUI-card/NAUI-card.vue'
export default {
    components: {NAUIcard}
}
```

在视图中使用

```
<NAUIcard listData="detail"></NAUIcard>
```

## 属性说明

listData(object)，需包含以下属性:

属性名 | 类型 | 说明
---|:--:|---
id | string | 卡片对应的id，可为空(用于跳转到详情页)
content | string | 卡片文字内容
img_url | array | 图片链接，默认显示第二张图片，可根据自己需要修改
user_name | string | 用户名
mark | boolean | 是否显示官方标志
type | string | 卡片类型或话题
points | string | 点赞数
show_times | string | 浏览次数
anony | boolean | 是否显示匿名标签/头像及匿名用户名
avatar_url | string | 头像链接
creat_time | string/number | 发帖时间


属性示例:

```
detail: {
        "id": "12",
        "content": "卡片文字内容",
        "img_url": [
            "http://img.nauzone.cn/78764bea5a2c8828b433d7b050bcc5a4",
            "http://img.nauzone.cn/8cfa5e52763ec60ab9ec933aa594a1c0",
            "http://img.nauzone.cn/778a955fdc252fb432c68f1247835b12",
            "http://img.nauzone.cn/4068d8d16c125a2ab76089166adf0903",
            "http://img.nauzone.cn/73eb04f0d7d426d96de6f356f181da5e"
        ],
        "user_name": "南审空间",
        "mark":true,
        "type": "表白墙",
        "points": "0",
        "show_times": "0",
        "anony": false,
        "avatarurl": "http://img.nauzone.cn/favicon11.png"
    },
```

## Tips

组件内包含了跳转详情和预览图片的事件，可根据自己的需求进行修改。(为避免点击报错，跳转事件已注释，请自行进行处理)

使用示例:

```
<template>
	<NAUIcard :listData="detail"></NAUIcard>
</template>

<script>
import NAUIcard from '@/components/NAUI-card/NAUI-card.vue';
export default {
	data() {
		return {
			detail: {
				id: '12',
				content: '卡片文字内容',
				img_url: [
					'http://img.nauzone.cn/78764bea5a2c8828b433d7b050bcc5a4',
					'http://img.nauzone.cn/8cfa5e52763ec60ab9ec933aa594a1c0',
					'http://img.nauzone.cn/778a955fdc252fb432c68f1247835b12',
					'http://img.nauzone.cn/4068d8d16c125a2ab76089166adf0903',
					'http://img.nauzone.cn/73eb04f0d7d426d96de6f356f181da5e'
				],
				user_name: '南审空间',
				mark: true,
				type: '表白墙',
				points: '0',
				show_times: '0',
				anony: false,
				avatarurl: 'http://img.nauzone.cn/favicon11.png',
				creat_time: '1552748677'
			}
		};
	},
	// 注册组件
	components: {NAUIcard},
	method: {}
};
</script>

<style></style>

```

*注:小白第一次在插件市场发布插件，虽然是封装的别人的样式，希望大家多多支持噢，如组件使用有问题请加我QQ:1468078360(备注:uniapp组件)联系噢。*


