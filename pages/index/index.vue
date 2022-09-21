<template>
	<view class="container">
		<uni-search-bar @confirm="search" :focus="true" v-model="keywords" @blur="blur" @focus="focus" @input="input"
			cancelButton="none" @clear="clear" bgColor="#eee">
		</uni-search-bar>
		<custom-waterfalls-flow ref="waterfallsFlowRef" :value="list" :column="2" imageKey="image" :columnSpace="2">
			<view class="item" v-for="(item,index) in list" :key="index" slot="slot{{index}}">
				<image :src="item.image"></image>
				<view class="title">{{item.title}}</view>
				<view class="desc">{{item.desc}}</view>
			</view>
		</custom-waterfalls-flow>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				keywords: '',
				list: [{
						image: 'https://via.placeholder.com/200x500.png/ff0000',
						title: '我是标题1',
						desc: '描述描述描述描述描述描述描述描述1'
					},
					{
						image: 'https://via.placeholder.com/200x200.png/2878ff',
						title: '我是标题2',
						desc: '描述描述描述描述描述描述描述描述2'
					},
					{
						image: 'https://via.placeholder.com/200x100.png/FFB6C1',
						title: '我是标题3',
						desc: '描述描述描述描述描述描述描述描述3'
					},
					{
						image: 'https://via.placeholder.com/200x300.png/9400D3',
						title: '我是标题4',
						desc: '描述描述描述描述描述描述描述描述4'
					},
					{
						image: 'https://via.placeholder.com/100x240.png/B0E0E6',
						title: '我是标题5',
						desc: '描述描述描述描述描述描述描述描述5'
					},
					{
						image: 'https://via.placeholder.com/140x280.png/7FFFAA',
						title: '我是标题6',
						desc: '描述描述描述描述描述描述描述描述6'
					},
					{
						image: 'https://via.placeholder.com/40x60.png/EEE8AA',
						title: '我是标题7',
						desc: '描述描述描述描述描述描述描述描述7'
					}
				]
			}
		},
		methods: {
			clear() {

			},
			input() {

			},
			focus() {

			},
			blur() {

			},
			search() {

			},
			// 刷新数据
			refresh() {
				this.list = []; // 赋值
				this.$refs.waterfallsFlowRef.refresh();
			}
		}
	}
</script>

<style lang="scss">
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;

		.item {
			padding: 10px 10px 20px;

			.title {
				line-height: 48px;
				font-size: 28px;
				color: #222;
			}

			.desc {
				font-size: 24px;
				color: #666;
			}
		}
	}
</style>
