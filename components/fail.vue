<style>
    .f_mengban{background: rgba(0,0,0,.5);width: 100%;height: 100%;position: fixed;top: 0;left: 0;z-index: 42;}
    .fail{
        width: 80%;
        position: fixed;
        border-radius:5px;
        top: 5.2rem;
        left: 10%;
        z-index: 45;
        background: rgba(246,246,246,.9);
        padding: 1rem;
    }
        .fail section{color: #fff;}
        .fail p{font-size: .7rem;color:#666;line-height: 1rem;}
    .failimg{background-image: url('data:image/png;base64,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');}
    .failimgbox{width: 4rem;height: 4rem;background-size: 100% 100%;margin: 1rem auto;}
</style>
<template>
    <div class="f_mengban" @click="cancelDone">
    </div>
    <section class="fail">
        <div class="failimg failimgbox">
        </div>
        <h3 class="text-center">提交失败</h3>
        <p class="text-center font-14">
            抱歉，可能是网络延时或其他原因，请再试一次！
        </p>
    </section>
</template>
<script type="text/javascript">
    export default{
        data(){
            return{

            }
        },
        methods:{
            cancelLayout:function(){
                this.$parent.isShowFail = false;
            },
            cancelDone:function(){
                this.cancelLayout();
            }
        },
        ready(){
            var self = this;
            // window.setTimeout(function(){
            //     self.cancelLayout();
            // },2000)
        }
    }
</script>
