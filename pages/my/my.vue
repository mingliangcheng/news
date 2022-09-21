<template>
	<view class="container">
		<uni-card :is-shadow="false" :border="false" margin="0">
			<view class="base-info">
				<view class="desc">
					<view class="nick-name">倾听他的事</view>
					<view class="signature">每个人都有快乐的事，你呢？</view>
				</view>
				<view>
					<image src="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg"></image>
				</view>
			</view>
			<view class="other-info">
				<view class="info-item">
					<text class="number">97</text>
					<text class="item-name">人气</text>
				</view>
				<view class="info-item">
					<text class="number">977</text>
					<text class="item-name">粉丝</text>
				</view>
				<view class="info-item">
					<text class="number">197</text>
					<text class="item-name">关注</text>
				</view>
			</view>
		</uni-card>
		<view class="middle-oprate">
			<view class="operate-btn">
				<uni-icons type="cloud-download" size="30"></uni-icons>
				<text>历史下载</text>
			</view>
			<view class="operate-btn">
				<uni-icons type="shop" size="30"></uni-icons>
				<text>审核进度</text>
			</view>
			<view class="operate-btn">
				<uni-icons type="headphones" size="30"></uni-icons>
				<text>帮助反馈</text>
			</view>
			<view class="operate-btn">
				<uni-icons type="gear" size="30"></uni-icons>
				<text>设置中心</text>
			</view>
		</view>
		<view class="works">
			<view class="top-wrap">
				<view class="my-works-btn">
					<view class="my-btn-wrap">
						<text>我的作品</text>
					</view>
					<view class="collect-btn">
						<uni-icons type="heart-filled" size="15" color="#ccc"></uni-icons>
					</view>
				</view>
				<view class="add-btn">
					<uni-icons type="plusempty" size="15" color="#ccc"></uni-icons>
				</view>
			</view>
		</view>
		<view class="works-list-wrap">
			<uni-card cover="https://fastly.jsdelivr.net/npm/@vant/assets/cat.jpeg" :is-shadow="false" :border="false" margin="0">
				<!-- <image slot='cover' style="width: 100%;" :src="cover"></image> -->
				<view class="uni-body">夜景</view>
				<view class="uni-desc">家具</view>
			</uni-card>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.container {
		::v-deep .uni-card {
			background-color: #f5f5f5;
		}
	}

	.base-info {
		display: flex;
		justify-content: space-between;

		.desc {
			.nick-name {
				font-size: 22px;
				font-weight: 700;
				color: #101010;
				margin-bottom: 10px;
			}

			.signature {
				color: #ccc;
			}
		}

		image {
			width: 100px;
			height: 100px;
			border-radius: 50%;
		}
	}

	.other-info {
		display: flex;

		.info-item {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			margin-right: 30px;

			.number {
				font-size: 18px;
				font-weight: 700;
				color: #101010;
				margin-bottom: 5px;
			}

			.item-name {
				font-size: 14px;
				color: #ccc;
			}
		}
	}

	.middle-oprate {
		padding: 15px;
		display: flex;

		.operate-btn {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			width: 25%;

			text {
				font-size: 12px;
			}
		}
	}

	.works {
		padding: 15px;

		.top-wrap {
			display: flex;
			justify-content: space-between;
			align-items: center;

			.my-works-btn {
				display: flex;
				align-items: center;

				.my-btn-wrap {
					display: flex;
					justify-content: center;
					align-items: center;
					background-color: #101010;
					color: #fff;
					width: 80px;
					height: 30px;
					border-radius: 15px;
					font-size: 14px;
					margin-right: 10px;
				}

				.collect-btn {
					width: 30px;
					height: 30px;
					border-radius: 50%;
					background-color: #ececec;
					display: flex;
					justify-content: center;
					align-items: center;
				}
			}

			.add-btn {
				width: 30px;
				height: 30px;
				border-radius: 50%;
				background-color: #ececec;
				display: flex;
				justify-content: center;
				align-items: center;
			}
		}
	}
	.works-list-wrap {
		padding: 15px;
		display: flex;
		::v-deep uni-card {
			width: calc(50% - 5px);
			&:nth-of-type(2n+1) {
				margin-right: 10px;
			}
		}
		::v-deep .uni-card {
			background-color: #fff;
		}
		.uni-body {
			font-size: 14px;
			color: #101010;
			font-weight: 700;
		}
		.uni-desc {
			font-size: 14px;
			color: #E2E2E2;
		}
	}
</style>
