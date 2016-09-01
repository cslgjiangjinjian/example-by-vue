<style>
    .mengban{background: rgba(0,0,0,.5);width: 100%;height: 100%;position: fixed;top: 0;left: 0;z-index: 30;}
    section.feedback {
        background-color: rgba(246,246,246,.9);
        border-radius:5px;
        left: 5%;
        position: fixed;
        z-index: 40;
        top: 5.2rem;
        width: 90%;
    }
        .feedback header{
            border-bottom: 1px solid rgba(0,0,0,.3);
            color: #000;
            font-size: .9rem;
            font-weight: 900;
            letter-spacing: -.45px;
            padding: .5rem 0;
        }
        section.feedback>div{padding: 0 .5rem;}
        section.feedback>div p{
            font-size: .7rem;
            line-height: 1rem;
            color:#666;
            letter-spacing: -.34px;
        }
        section.feedback>div h3{
            font-size: .7rem;
            line-height: 1rem;
            color:#333;
            font-weight: 500;
            letter-spacing: -.3px;
            margin: .5rem 0;
        }
        section.feedback>div h5{
            font-size: .6rem;
            line-height: 1rem;
            color:#7d7d7d;
            font-weight: 500;
            letter-spacing: .07px;
            margin: 0 0 .3rem 0;
        }
        .feedback .textarea,.feedback .textarea textarea{
            width: 100%;
        }
        .feedback .textarea textarea{
            border: none;
            resize: none;
            line-height: 1rem;
            outline: none;
            padding: .5rem;
            height: 6rem;
            background: none;
            font-size: .8rem;
        }
        .feedback footer{
            border-top: 1px solid rgba(0,0,0,.3);
        }
        .feedback footer>div{width: 50%;color: #007AFF;font-size: .85rem;line-height: 1rem;padding: .6rem 0;letter-spacing: -.4px;font-weight: 900;}
        .feedback footer .cancel-button{border-right: 1px solid rgba(0,0,0,.3);}
</style>
<template id="feedback">
    <div>
        <div class="mengban">
        </div>
        <section class="feedback">
            <header class="text-center">
                问题反馈
            </header>
            <div class="">
                <p>
                    *请输入您在销售中遇到的问题，相关同事会及时作出应答。
                </p>
                <h3>所遇问题:</h3>
                <div class="textarea">
                    <textarea class="text-left" name="name" v-model="questions"></textarea>
                </div>
                <h5 class="text-right">0/50</h5>
            </div>
            <footer class="clear">
                <div class="cancel-button left text-center" @click="cancel">
                    取消
                </div>
                <div class="left text-center" @click="submit">
                    提交
                </div>
            </footer>
        </section>
    </div>

</template>
<script type="text/javascript">
import API from "../models/api"
var $ = require('jquery');
    export default{
        components:{

        },
        data(){
            return {
                questions:""
            }
        },
        methods:{
            cancel:function(){
                //isShowFeedBack from header.vue
                this.$parent.isShowFeedBack = false;
            },
            submit:function(){
                var self = this;
    			var url = API.questionsOperation;
                var data={
                    "questions":self.questions,
                    "type":0
                }
    			$.ajax({
    				type:"post",
    				url:url,
                    data:data,
                    dataType:"json",
    				success:function(msg){
    					if(msg.code ==200){
    						self.$parent.isShowSuccess = true;
    					}else{
    						self.$parent.isShowFail = true;
    					}
                        self.$parent.isShowFeedBack = false;
    				},
    				error:function(e){
                        self.$parent.isShowFeedBack = false;
                        self.$parent.isShowFail = true;
    					console.log(e);
    				}
    			})
                //this.$parent.isShowSuccess = true;
                //this.$parent.isShowFail = true;
            }
        },
        ready(){

        }
    }
</script>
