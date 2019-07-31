<template>
	<view>
		<view class="btn-group">
			<view>取消</view>
			<view class="btn-pulish" @click="pulish">发布</view>
		</view>
		<view class="tag">
			<uni-list-item title="# 瞬间标签"></uni-list-item>
		</view>
		<view class="text-edit">
			<textarea class="text-area" placeholder="为您美好的瞬间描述下吧..."></textarea>
		</view>
		<view class="img-group">
			<image-drag-sort :list="images"></image-drag-sort>
		</view>
		<view class="outher">
			<uni-list-item title="瞬间位置"></uni-list-item>
			<uni-list-item title="可见范围"></uni-list-item>
			<uni-list-item title="瞬间权限"></uni-list-item>
		</view>
	</view>
</template>

<script>
	import imageDragSort from '@/components/image-drag-sort/'
	import {uniListItem } from '@dcloudio/uni-ui'
	
	export default {
		components: {
			imageDragSort,
			uniListItem,
		},
		data() {
			return {
				images: []
			}
		},
		methods: {
			pulish(){
				uni.showLoading({
					title: "美好瞬间推送"
				})
			},
		}
	}
</script>

<style>
	.btn-group{
		height: 60rpx;
		line-height: 60rpx;
		display: flex;
		justify-content: space-between;
		padding: 10rpx 30rpx;
		font-size: 14px;
	}
	.btn-pulish{
		background-color: #00CCFF;
		width: 120rpx;
		height: 60rpx;
		line-height: 60rpx;
		border-radius: 10rpx;
		text-align: center;
		color: #FFFFFF;
		font-weight: 500;
	}
	
	.text-edit{
		height: 300upx;
		width: 750upx;
	}
	.text-area{
		width: 100%;
		padding: 30rpx;
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		font-size: 14px;
	}
	
	.outher{
		
	}
	.uni-list-item__content-title{
		font-size: 14px!important;
	}
	
</style>
