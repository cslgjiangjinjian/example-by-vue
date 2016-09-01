<style>
    .d_table .d_th {background-color: #BAC2C7;font-size: .7rem;letter-spacing: -.34px;line-height: 1rem;padding: .6rem 0;text-align: center;color: #333;font-weight: 900;}
    .d_table .d_tr {background-color: #fff;font-size: .7rem;letter-spacing: -.34px;padding: .6rem 0;text-align: center;border-bottom: 1px solid #ddd;color: #7d7d7d;}
    .d_table .d_tr .d_td{line-height: 1rem;}
    .d_table .d_th .d_td:nth-of-type(1),.d_table .d_tr .d_td:nth-of-type(1){width: 20%;float: left;}
    .d_table .d_th .d_td:nth-of-type(2),.d_table .d_tr .d_td:nth-of-type(2){width: 40%;float: left;}
    .d_table .d_th .d_td:nth-of-type(3),.d_table .d_tr .d_td:nth-of-type(3){width: 40%;float: left;}
</style>
<template id="">
    <div class="">
        <section class="d_table">
            <div class="d_th clear">
                <div class="d_td">
                    模块
                </div>
                <div class="d_td">
                    他们的劣势
                </div>
                <div class="d_td">
                    我的优势
                </div>
            </div>
            <ul class="d_tbody">
                <li class="d_tr clear" v-for="item in dataList">
                    <div class="d_td" v-text="item.modelName"></div>
                    <div class="d_td" v-text="item.disadvantages"></div>
                    <div class="d_td" v-text="item.advantages"></div>
                </li>
            </ul>
        </section>
    </div>
</template>
<script type="text/javascript">
import API from "../models/api"
var $ = require('jquery');
    export default{
        data(){
            return {
                dataList:[]
            }
        },
        methods:{
            getDetail:function(id){
                console.log('详情ID：'+id);
                var self = this;
    			var url = API.bfAnalysis+"?businessFriendsId="+id;
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
            console.log('分析详情')
            var id = window.location.hash.split('#!/')[1].split('/')[1];
            this.getDetail(id);
        }
    }
</script>
