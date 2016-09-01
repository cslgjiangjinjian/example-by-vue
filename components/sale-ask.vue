<style type="text/css">
	.sale-ask{float: left;width: 100%;min-height: 300px;}
		.sale-ask-list{background-color: #fff;}
			.sale-ask-list ul li{font-size: .7rem; padding: .5rem 1rem;border-top: 1px solid #ddd;border-bottom: 1px solid #ddd;}
			.sale-ask-list ul li h3{padding-bottom: 1rem;}
			.sale-ask-list ul li p{line-height: 1rem;color: #666;}
	.sale-ask .search{padding: .5rem 0;}
	.sale-ask .search>div{width: 90%;margin: 0 auto;border-radius: 5px;}
	.sale-ask .search>div>input{width: 100%;height: 1.4rem;line-height: 1.4rem;padding: 2px 5px;background: #fff;border-radius: 5px;border: none;}
</style>
<template>
	<div class="sale-ask">
		<div class="search">
			<div class="">
				<input type="text" placeholder="搜索" value="">
			</div>
		</div>
		<section class="sale-ask-list">
			<ul>
				<li v-for="item in dataList">
					<h3 v-text="item.questions"></h3>
					<p v-text="item.answers"></p>
				</li>
			</ul>
		</section>
	</div>
</template>
<script type="text/javascript">
import API from "../models/api"
var $ = require('jquery');
	export default {
		data(){
			return {
				dataList:[]
			}
		},
		methods:{
			get:function(){
				console.log('sale-ask');
				var self = this;
				var url = API.getQuestions+"?state=1&page=0&size=10";
				$.ajax({
					type:"get",
					url:url,
					success:function(msg){
						if(msg.code ==200){
							self.dataList = msg.data.content;
						}else{
							alert(msg.description);
						}
					},
					error:function(e){
						console.log(e);
					}
				})
			}
		},
		ready(){
			console.log('问题列表')
			this.get();
		}
	}
</script>
