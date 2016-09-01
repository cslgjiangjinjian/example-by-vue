<template>
	<div class="app">
		<com-header></com-header>
		<com-main></com-main>
		<com-footer v-if="isShowFooter"></com-footer>
	</div>
</template>

<script>
	import ComHeader from './Header.vue'
	import ComFooter from './Footer.vue'
	import ComMain from './Main.vue'
	export default {
		components:{
			ComHeader,
			ComFooter,
			ComMain
		},
		data(){
			return {
				ROUTE:'',
				HEAD:'',
				isShowFooter:true
			}
		},
		methods:{
		},
		watch:{
			"ROUTE":function(newval){
				if(newval=='ysfx-d'){
					this.isShowFooter = false;
				}else{
					this.isShowFooter = true;
				}
			}
		}
	}
</script>
