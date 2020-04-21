<template>
    <div>
        <div class="wrap"></div>
        <div class="bg" :style="{position: 'fixed',top: wanwanTop+'px',right: 380+'px'}"></div>
        <div class="bg2" :style="{position: 'fixed',top:zhangyuTop+'px',left:285+'px'}"></div>
        <div class="bg3" :style="{position:'fixed',top:title1+'px',left: 700+'px'}"></div>
        <div class="bg4" :style="{position:'fixed',top:title2+'px',left:985+'px'}"></div>
        <div class="bg5" :style="{position:'fixed',top:title3+'px',left:866+'px'}"></div>
        <div class="bg6" :style="{position:'fixed',top:title4+'px',left:800+'px'}"></div>
<!--        <div class="bg7" :style="{position:'fixed',top:fish+'px',left:330+'px'}"></div>-->
        <img src="../assets/shanhu.png" style="position: absolute;top: 639px;left: 0;width: 100%;z-index: 1" >
        <img src="../assets/shitou.png" style="position:absolute;top:2000px;left: 0;width: 100%;z-index: 2">
        <img src="../assets/fish.png" :style="{position:'absolute',top:fish+'px',left: 330+'px'}">
        <div class="bg7"></div>
        <img src="../assets/dimian.png" style="position: absolute;left: 0;top: 2900px;width: 100%;height: 330px">
        <img src="../assets/first.png" style="position: absolute;left: 0;top: 2000px;width: 100%;height: 330px">
    </div>
</template>

<script>
    export default {
        name: "home",
        data(){
            return{
                wanwanTop:88,
                zhangyuTop:465,
                title1:480,
                title2:570,
                title3:692,
                title4:752,
                fish:550,
            }
        },
        mounted() {
            console.log(window.innerHeight);
            // chrome and ie
            window.addEventListener('mousewheel',this.handleScroll,false)
            // firefox
            window.addEventListener("DOMMouseScroll",this.handleScroll,false)
        },
        methods:{
            handleScroll(e){
                //     //htmlHeight 是网页的总高度
                var htmlHeight = document.body.scrollHeight || document.documentElement.scrollHeight;
                //     //clientHeight是网页在浏览器中的可视高度，
                var clientHeight = document.body.clientHeight || document.documentElement.clientHeight;
                //     //scrollTop是浏览器滚动条的top位置，
                var scrollTop = document.body.scrollTop || document.documentElement.scrollTop;
                console.log('网页总高度--',htmlHeight,'网页可视高度--',clientHeight,'滚动条的高度--',scrollTop)
                console.log(e);
                // console.log('鼠标滚动了')
                if(e.deltaY>0){
                    console.log('鼠标下滚top---')
                    this.wanwanTop -=50
                    this.zhangyuTop -=50
                    this.title1 -=40
                    this.title2 -=40
                    this.title3 -=40
                    this.title4 -=40
                    this.fish -=40
                    console.log(this.wanwanTop);
                }else {
                    console.log('鼠标上滚top+++')
                    this.wanwanTop +=50
                    this.zhangyuTop +=50
                    this.title1 +=40
                    this.title2 +=40
                    this.title3 +=40
                    this.title4 +=40
                    this.fish +=30
                    console.log(this.wanwanTop);
                    //如果鼠标到顶则将top重置为88
                    if(this.wanwanTop>88){
                        this.wanwanTop = 88
                        this.zhangyuTop = 465
                        this.title1 = 480
                        this.title2 = 570
                        this.title3 = 692
                        this.title4 = 752
                        this.fish = 550
                    }
                }
            }
        },

    }
</script>

<style scoped>
    .wrap{
        background: url("../assets/bimg.png");
        /*background-attachment: fixed;*/
        width: 100%;
        height:3247px;
        /*position: fixed;*/
        /*left: 0;*/
        /*top: 0;*/
    }
    .bg{
        background:url("../assets/wanwan.gif") no-repeat;
        width: 480px;
        height: 480px;
        background-size: cover;
        z-index: 99;
    }
    .bg2{
        background:url("../assets/zhangyu.gif") no-repeat;
        width: 480px;
        height: 480px;
        background-size: cover;
        z-index: 99;
    }
    .bg3{
        background: url("../assets/MOONBAY.png") no-repeat;
        background-size: cover;
        width: 425px;
        height: 65px;
        z-index: 99;
    }
    .bg4{
        background: url("../assets/WAKE.png") no-repeat;
        background-size: cover;
        width: 226px;
        height: 67px;
        z-index: 99;
    }
    .bg5{
        background: url("../assets/go.png") no-repeat;
        background-size: cover;
        width: 185px;
        height: 44px;
        z-index: 99;
    }
    .bg6{
        background: url("../assets/world.png") no-repeat;
        background-size: cover;
        width: 321px;
        height: 44px;
        z-index: 99;
    }
    .bg7{
        background:url("../assets/house.png")no-repeat;
        background-size: cover;
        width: 450px;
        height: 450px;
        position: absolute;
        left: 0;
        top: 2300px;
        z-index: 3;
    }

</style>