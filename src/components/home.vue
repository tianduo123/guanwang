<template>
    <div>
        <div class="shanhu" :style="{top:shanhu_t+'px'}"></div>
        <div class="zzb" :style="{top:zzb_t+'px'}"></div>
        <div class="shitou" :style="{top:shitou_t+'px'}"></div>
        <div class="haima" :style="{top:haima_t+'px'}"></div>
        <div class="house" :style="{top:house_t+'px'}"></div>
        <div class="hailuo" :style="{top:hailuo_t+'px'}"></div>
    </div>
</template>

<script>
    export default {
        name: "home",
        data(){
            return{
                i:0,
                shanhu_t:650,
                shitou_t:2500,
                zzb_t:1570,
                haima_t:2300,
                house_t:4400,
                hailuo_t:4400
            }
        },
        mounted() {
            window.addEventListener('scroll',this.handleScroll,true)
        },
        methods:{
            handleScroll(){
                //滚动条距离顶部距离
                var scrollTop = window.pageYOffset||document.documentElement.scrollTop||document.body.scrollTop
                //当前窗口的可视高度
                var windowHeight = document.documentElement.clientHeight||document.body.clientHeight
                //滚动条内容的总高度
                var scrollHeight = document.documentElement.scrollHeight||document.body.scrollHeight;
                if(scrollTop+windowHeight!=scrollHeight){
                    // console.log('滚动到底')
                    var scroll = scrollTop - this.i
                    this.i = scrollTop
                    if(scroll<0){
                        console.log('up')
                        this.shanhu_t += 5
                        this.zzb_t += 5
                        this.shitou_t += 10
                        this.haima_t += 10
                        this.house_t += 30
                        this.hailuo_t +=30
                    }else {
                        console.log('down')
                        this.shanhu_t -= 5
                        this.shitou_t -= 10
                        this.zzb_t -= 5
                        this.haima_t -= 10
                        this.house_t -= 30
                        this.hailuo_t -=30

                    }
                }else {
                    console.log('滚动到底了top值不在变化')
                }

                if(scrollTop==0){
                    console.log('滚动到顶')
                    this.shanhu_t = 650
                    this.shitou_t = 2500
                    this.zzb_t = 1570
                    this.haima_t = 2300
                    this.house_t = 4400
                    this.hailuo_t = 4400
                }
            }
        }
    }
</script>

<style scoped>
    .shanhu{
        position: absolute;
        left: 0;
        /*top:650px;*/
        background: url("../assets/shanhu.png");
        width: 100%;
        height: 1800px;
        background-repeat: no-repeat;
        background-size: cover;
    }
    .shitou{
        position: absolute;
        left: 0;
        /*top: 2200px;*/
        background: url("../assets/shitou.png");
        width: 100%;
        height: 700px;
        background-size: cover;
        background-repeat: no-repeat;
    }
    .zzb{
        position: absolute;
        left: 180px;
        /*top: 1570px;*/
        background: url("../assets/zzb.gif");
        width: 400px;
        height: 400px;
        background-size: cover;
        background-repeat: no-repeat;
    }
    .haima{
        position: absolute;
        right: 120px;
        background: url("../assets/seahorse.gif");
        width: 300px;
        height: 320px;
        background-size: cover;
        background-repeat: no-repeat;
    }
    .house{
        position: absolute;
        left: 0;
        background: url("../assets/house.png");
        width: 400px;
        height: 400px;
        background-size: cover;
        background-repeat: no-repeat;
    }
    .hailuo{
        position: absolute;
        left: 500px;
        background: url("../assets/hailuo.png");
        width: 730px;
        height: 780px;
        background-size: 500px 500px;
        background-repeat: no-repeat;
    }
</style>