<style>
    .s_mengban{background: rgba(0,0,0,.5);width: 100%;height: 100%;position: fixed;top: 0;left: 0;z-index: 42;}
    .success{
        width: 80%;
        position: fixed;
        border-radius:5px;
        top: 5.2rem;
        left: 10%;
        z-index: 45;
        background: rgba(246,246,246,.9);
        padding: 1rem;
    }
        .success section{color: #fff;}
        .success p{font-size: .7rem;color:#666;line-height: 1rem;}
    .successimg{background-image: url('data:image/png;base64,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');}
    .successimgbox{width: 4rem;height: 4rem;background-size: 100% 100%;margin: 1rem auto;}

</style>
<template>
    <div class="s_mengban" @click="cancelDone">
    </div>
    <section class="success">
        <div class="successimg successimgbox"></div>
        <h3 class="text-center">提交成功</h3>
        <p class="text-center font-14">
            相关同事会及时作出响应，请留意销售问答资料的更新！
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
                this.$parent.isShowSuccess = false;
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
