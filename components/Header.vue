<style type="text/css">
	.header{width: 100%;padding: .5rem;background-color: #222;color: #fff;position: fixed;z-index: 100;}
	.title{margin: 0 3.5rem;font-size: .9rem;line-height: 1rem;}
	.back{position: absolute;top: .5rem;left: .5rem;font-size:.75rem;line-height: 1rem;padding-left: .5rem;}
	.back:after{content:"<";position: absolute;left: 0;top: 0;}
	.feed{position: absolute;top: .5rem;right: .5rem;font-size:.75rem;line-height: 1rem;}
</style>
<template>
	<header class="header">
		<span class="back" @click="back">
			关闭
		</span>
		<div class="title text-center" v-text="head">
		</div>
		<span class="feed" v-if="isShowFeedBtn" @click="feed">
			问题反馈
		</span>
	</header>
	<feed-back v-if="isShowFeedBack"></feed-back>
	<success v-if="isShowSuccess"></success>
	<fail v-if="isShowFail"></fail>
</template>
<script type="text/javascript">
	import FeedBack from './feedback.vue'
	import Success from './success.vue'
	import Fail from './fail.vue'
	export default {
		components:{
			FeedBack,
			Success,
			Fail
		},
		data(){
			return {
				head:'销售问答',
				isShowFeedBtn:true,//显示问题反馈按钮
				isShowFeedBack:false,//显示问题反馈
				isShowSuccess:false,//显示成功
				isShowFail:false//显示失败
			}
		},
		methods:{
			back:function(){
				console.log('back');
				window.history.go(-1);
			},
			feed:function(){
				this.isShowFeedBack = true;
			}
		},
		ready(){
		},
		watch:{
			"$parent.ROUTE":function(newval){
				if(newval=='ysfx-d'){
					this.isShowFeedBtn =false;
				}else{
					this.isShowFeedBtn =true;
				}
				switch(newval){
					case "xswd":
						this.head = "销售问答";
						break;
					case "ysfx":
						this.head="友商分析";
						break;
					default:
						this.head = this.$parent.HEAD;
						break;
				}
			}
		}
	}
</script>
