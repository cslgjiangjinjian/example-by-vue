<style>
	.business-analysis{float: right;width: 100%;}
    .ba-list{background-color: #fff;}
	    .ba-list li{line-height: 2.2rem;color: #000;border-bottom: 1px solid #ddd;padding: 0 1rem;position: relative;}
	    .ba-list li:after{content:">";position: absolute;right: 1rem;color: #000;}
</style>
<template>
	<div class="business-analysis">
        <section class="ba-list">
            <ul>
    		    <li v-for="item in dataList" v-text="item.systemName" @click="toDetail(item)"></li>
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
        toDetail:function(obj){
            window.location.hash = "#!/ysfx-d/"+obj.friendsId;
			this.$parent.$parent.HEAD = obj.systemName;
			localStorage.t = obj.systemName;
			console.log(this.$parent.$parent.HEAD);

        },
		get:function(){
			console.log('sale-ask');
			var self = this;
			var url = API.businessFriendsList+"?page=0&size=10";
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
		console.log('分析列表')
		this.get();
	}
}
</script>
