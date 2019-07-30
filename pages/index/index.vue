<template>
	<view class="content">
		<view :style="'height: '+h+'px; overflow-y: auto; background-color:#f6f9fe;'">
			<an-card :listData="item" v-for="(item, index) in lists" :key="index"></an-card>
		</view>
	</view>
</template>

<script>
	import anCard from '@/components/an-card/an-card.vue'
	
	export default {
		components: {
			anCard
		},
		data() {
			return {
				h: uni.getSystemInfoSync().windowHeight,
				lists: [
					{
						"id": "12",
						"content": "我家这狗咋地了",
						"img_url": [
							"http://img5.imgtn.bdimg.com/it/u=3987907653,720009510&fm=26&gp=0.jpg",
							"http://images.17173.com/2013/news/2013/07/11/hxz0711rsyz01.jpg",
							"http://photocdn.sohu.com/20111207/Img328215620.jpg",
							"http://pic22.nipic.com/20120621/5750160_084359248000_2.jpg"
						],
						"user_name": "南审空间",
						"mark":true,
						"type": "表白墙",
						"points": "0",
						"show_times": "0",
						"anony": false,
						"avatarurl": "http://img.nauzone.cn/favicon11.png"
					},
					{
						"id": "1",
						"content": "我的打开就服你打开",
						"img_url": [
							"http://img5.imgtn.bdimg.com/it/u=3987907653,720009510&fm=26&gp=0.jpg",
							"http://images.17173.com/2013/news/2013/07/11/hxz0711rsyz01.jpg",
							"http://photocdn.sohu.com/20111207/Img328215620.jpg",
							"http://pic22.nipic.com/20120621/5750160_084359248000_2.jpg"
						],
						"user_name": "张三",
						"mark":true,
						"type": "天气",
						"points": "0",
						"show_times": "0",
						"anony": false,
						"avatarurl": "http://img.nauzone.cn/favicon11.png"
					},
					{
						"id": "1",
						"content": "东山口if康复科",
						"img_url": [
							"http://img5.imgtn.bdimg.com/it/u=3987907653,720009510&fm=26&gp=0.jpg",
							"http://images.17173.com/2013/news/2013/07/11/hxz0711rsyz01.jpg",
							"http://photocdn.sohu.com/20111207/Img328215620.jpg",
							"http://pic22.nipic.com/20120621/5750160_084359248000_2.jpg"
						],
						"user_name": "张三",
						"mark":true,
						"type": "天气",
						"points": "0",
						"show_times": "0",
						"anony": false,
						"avatarurl": "http://img.nauzone.cn/favicon11.png"
					}
				],
				info: [{
					content: '内容 A'
				}, {
					content: '内容 B'
				}, {
					content: '内容 C'
				}, {
					content: '内容 C'
				}],
				current: 0,
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
