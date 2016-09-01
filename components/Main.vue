<style type="text/css">
	.main{
		background-color: #eee;
		padding-top: 2rem;
	}
	.clear{overflow: hidden;}
	.nav{background-color: #fff;color: #000;}
</style>
<template>
	<div class="main">
		<div>
			<sale-ask v-if="showRoute=='xswd'"></sale-ask>
			<business-analysis v-if="showRoute=='ysfx'"></business-analysis>
			<business-analysis-detail v-if="showRoute=='ysfx-d'"></business-analysis-detail>
		</div>
	</div>
</template>
<script type="text/javascript">

//import MainLeft from './main-left.vue'
import BusinessAnalysis from './business-analysis.vue'
import BusinessAnalysisDetail from './business-analysis-detail.vue'
import SaleAsk from './sale-ask.vue'

	export default {
		components:{
			SaleAsk,
			BusinessAnalysis,
			BusinessAnalysisDetail
		},
		data(){
			return {
				content:'this is main content',
				showRoute:'',
				showHead:'',
			}
		},
		ready(){
			var self = this;
			self.showHead = self.$parent.HEAD;
			window.onhashchange = function(){
				var hash = window.location.hash;
				if(!!hash.split('#!/')[1]){
					hash = hash.split('#!/')[1].split('/')[0];
				}else{
					hash = 'xswd';
				}
				self.showRoute = hash;
				self.$parent.ROUTE = hash;
				console.log('onhashchange')
			}
			window.onload = function(){
				var hash = window.location.hash;
				if(!!hash.split('#!/')[1]){
					hash = hash.split('#!/')[1].split('/')[0];
				}else{
					hash = 'xswd';
				}
				console.log("hash："+hash)
				if(hash=='ysfx-d'){
					self.$parent.HEAD = localStorage.t;
				}
				console.log('onload')
				self.showRoute = hash;
				self.$parent.ROUTE = hash;
			}
		}
	}
</script>
