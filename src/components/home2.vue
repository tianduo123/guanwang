<template>
    <div class="bgimg">
        <div class="bg1" :style="{top:bg1top+'px'}"></div>
        <div class="bg2" :style="{top:bg2top+'px'}"></div>
        <div class="bg3" :style="{top:bg3top+'px'}"></div>
        <div class="bg4" :style="{top:bg4top+'px'}"></div>
        <div class="bg5" :style="{top:bg5top+'px'}"></div>
        <div class="bg6" :style="{top:bg6top+'px'}"></div>
<!--        <div class="content" style="margin-top: 1500px">-->
<!--            <div class="left">-->
<!--                <div class="left_t">-->
<!--                    <span style="font-weight: bold;font-size: 24px">品牌优势</span>-->
<!--                    <span style="font-size: 20px">Moonbay Brand</span>-->
<!--                    <span style="font-size: 20px">Advantago</span>-->
<!--                </div>-->
<!--                <div class="left_b">-->
<!--                    <span v-for="(item,index) in youshiList" :class="{active:item.active}">-->
<!--                        {{item.name}}-->
<!--                    </span>-->
<!--                </div>-->
<!--            </div>-->
<!--            <div class="right" v-show="show">-->
<!--                <div>{{}}</div>-->
<!--            </div>-->
<!--        </div>-->
        <div class="bg7" :style="{top:bg7top+'px'}"></div>
        <div class="bg8" :style="{top:bg8top+'px'}"></div>
        <div class="bg9" :style="{top:bg9top+'px'}"></div>
        <div class="bg10" :style="{top:bg10top+'px'}"></div>
        <div class="bg11" :style="{top:bg11top+'px'}"></div>
        <div class="bg12" :style="{top:bg12top+'px'}"></div>
        <div class="bg13" :style="{top:bg13top+'px'}"></div>
<!--        <div class="bg14" :style="{top:bg14top+'px'}"></div>-->
    </div>

</template>

<script>
    export default {
        name: "home2",
        data(){
            return{
                youshiList:[
                    {name:'ERP门店管理系统支持',active:true},
                    {name:'SOP运营标准化管理体系支持',active:false},
                    {name:'品牌标准化管理体系支持',active:false},
                    {name:'售后服务标准化支持',active:false},
                    {name:'自主研发产品系列',active:false},
                ],
                show:false,
                bg1top:95,
                bg2top:309,
                bg3top:300,
                bg4top:400,
                bg5top:558,
                bg6top:617,
                bg7top:700,
                bg8top:1300,
                bg9top:1800,
                bg10top:2000,
                bg11top:1500,
                bg12top:1700,
                bg13top:1800,
                // bg14top:2300,
            }
        },
        methods:{
            // handleScroll(e){
            //     console.log(e);
            //     if(e.wheelDelta>0){
            //         console.log('IE、Chrome鼠标滑轮向上滚动')
            //     }
            //     if(e.wheelDelta<0){
            //         console.log('IE、Chrome鼠标滑轮向下滚动')
            //     }
            //     if(e.detail>0){
            //         console.log('Firefox鼠标滑轮向下滚动')
            //     }
            //     if(e.detail<0){
            //         console.log('Firefox鼠标滑轮向上滚动')
            //     }
            // },

            //滚动条事件
            // handler(){
            //     /**
            //      *  scrollTop -- 滚动条滚动高度
            //      *
            //      */
            //     var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
            //     // var scroll = scrollTop - this.i
            //     // this.i = scrollTop
            //     // console.log(scrollTop,this.i,scroll);
            //     // if(scroll<0){
            //     //     console.log('up')
            //     //     this.bg12_top += 5
            //     // }else {
            //     //     console.log('down')
            //     //     this.bg12_top -= 5
            //     // }
            // }

            handleScroll(e){
                // var scrollTop = document.body.scrollTop || document.documentElement.scrollTop;
                console.log(e);
                // console.log('鼠标滚动了')
                if(e.deltaY>0){
                    console.log('鼠标下滚top---')
                    this.bg1top -= 100
                    this.bg2top -= 100
                    this.bg3top -= 60
                    this.bg4top -= 60
                    this.bg5top -= 60
                    this.bg6top -= 60
                    this.bg7top -= 200
                    this.bg8top -= 200
                    this.bg9top -= 200
                    this.bg10top -= 200
                    this.bg11top -= 200
                    this.bg12top -= 200
                    this.bg13top -= 200
                    // this.bg14top -= 200
                }else {
                    console.log('鼠标上滚top+++')
                    this.bg1top += 100
                    this.bg2top += 100
                    this.bg3top += 60
                    this.bg4top += 60
                    this.bg5top += 60
                    this.bg6top += 60
                    this.bg7top += 200
                    this.bg8top += 200
                    this.bg9top += 200
                    this.bg10top += 200
                    this.bg11top += 200
                    this.bg12top += 200
                    this.bg13top += 200
                    this.bg14top += 200

                    //如果鼠标到顶则将top重置为190
                    console.log(this.bg1top)
                    if(this.bg1top>95){
                        this.bg1top = 95
                        this.bg2top = 309
                        this.bg3top = 300
                        this.bg4top = 400
                        this.bg5top = 558
                        this.bg6top = 617
                        this.bg7top = 700
                        this.bg8top = 1300
                        this.bg9top = 1800
                        this.bg10top = 2000
                        this.bg11top = 1500
                        this.bg12top = 1700
                        this.bg13top = 1800
                        // this.bg14top = 2300
                    }
                }

            }

        },
        mounted() {
            //  Firefox
            window.addEventListener('DOMMouseScroll',this.handleScroll,false)
            //  其他浏览器
            window.addEventListener('mousewheel',this.handleScroll,false)

            //监听滚动条
            // window.addEventListener('scroll',this.handler,true)
            // console.log(this.$refs.wanwan);

            /**
             * 由近到远层数 z-index由大到小
             *  第一层 -- 第一层珊瑚
             *  第二层 -- 地面、第二层珊瑚、海星
             *  第三层 -- 海螺、花蕊珊瑚、小房子
             *  第四次 -- 石头、海马
             *  第五层 -- 鱼群
             *  第六层 -- 珊瑚背景、珍珠贝
             */
        }
    }
</script>

<style scoped>
    .bgimg{
        width: 100%;
        height: 2000px;
    }
    .bg1{
        background-repeat: no-repeat;
        background: url("../assets/wanwan.gif");
        position: fixed;
        right: 395px;
        /*top: 95px;*/
        width: 400px;
        height: 400px;
        background-size: 378px 400px;
    }
    .bg2{
        background: url("../assets/zhangyu.gif");
        position: fixed;
        left: 283px;
        /*top: 309px;*/
        width: 100%;
        height: 700px;
        background-size: 650px 647px;
        background-repeat: no-repeat;
        z-index: 2;
    }
    .bg3{
        background: url("../assets/MOONBAY.png");
        position: fixed;
        left: 700px;
        /*top: 300px;*/
        width: 100%;
        height: 700px;
        background-size: 420px 75px;
        background-repeat: no-repeat;
        z-index: 3;
    }
    .bg4{
        background: url("../assets/WAKE.png");
        position: fixed;
        left: 987px;
        /*top: 440px;*/
        width: 100%;
        height: 100px;
        background-size: 230px 70px;
        background-repeat: no-repeat;
        z-index: 3;
    }
    .bg5{
        background: url("../assets/go.png");
        position: fixed;
        left: 870px;
        /*top: 558px;*/
        width: 100%;
        height: 100px;
        background-size: 185px 45px;
        background-repeat: no-repeat;
        z-index: 3;
    }
    .bg6{
        background: url("../assets/world.png");
        position: fixed;
        left: 800px;
        /*top: 617px;*/
        width: 100%;
        height: 100px;
        background-size: 320px 50px;
        background-repeat: no-repeat;
        z-index: 3;
    }
    .content{

        width: 1200px;
        height: 600px;
        /*background: #6d6d6d;*/
        margin: 30px auto;
        display: flex;
    }
    .left{
        width: 50%;
        height: 100%;
        display: flex;
        flex-direction: column;
        box-sizing: border-box;
        padding-left: 40px;
        padding-top: 40px;
        padding-bottom: 40px;
        background: rgba(0,0,0,.3);

    }
    .left_t{
        display: flex;
        flex-direction: column;
        color: white;
        height: 20%;
    }
    .active{
        color: yellow;
    }
    .left_b{
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        height: 80%;
        color: white;
    }
    .right{
        width: 50%;
        height: 100%;
        background: rgba(0,0,0,.3);

    }
    .bg7{
        background: url("../assets/shanhu.png");
        position: fixed;
        left: 0;
        /*top: 700px;*/
        width: 100%;
        height: 1500px;
        background-repeat: no-repeat;
        background-size: 100% 100%;
    }
    .bg8{
        background: url("../assets/zzb.gif");
        position: fixed;
        background-repeat: no-repeat;
        background-size: 100% 100%;
        width: 355px;
        height: 355px;
        /*top: 1000px;*/
        left: 122px;
    }
    .bg9{
        background:url("../assets/shitou.png");
        position: fixed;
        left: 0;
        /*top: 1500px;*/
        width: 100%;
        height: 400px;
        background-size: 100% 100%;
    }
    .bg10{
        background: url("../assets/house.png");
        position: fixed;
        left: 0;
        /*top: 1500px;*/
        width: 500px;
        height: 400px;
        background-size: 100% 100%;
    }
    .bg11{
        background:url("../assets/seahorse.gif");
        position: fixed;
        right: 50px;
        /*top: 1000px;*/
        width: 500px;
        height: 400px;
        background-size: 100% 100%;
    }
    .bg12{
        background:url("../assets/hailuo.png");
        position: fixed;
        left: 500px;
        width: 800px;
        height: 800px;
        background-size: 100% 100%;
        z-index: -1;
    }
    .bg13{
        background: url("../assets/shanhu2.png");
        position: fixed;
        right: 0;
        background-size: 100% 100%;
        width: 50%;
        height: 800px;
    }
    .bg14{
        background: url("../assets/dimian.png");
        position: fixed;
        left: 0;
        /*top:2000px;*/
        width: 100%;
        height: 200px;
        background-size: 100% 100%;
    }

</style>