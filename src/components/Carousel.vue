<template>
    <div class="carousel-box">
      <el-carousel height="380px" trigger="click" :interval="4000" pause-on-hover>
        <el-carousel-item v-for="item in imgList" :key="item.id">
            <a target="_blank" rel="nofollow" :href=item.href class="a-dis" 
            :style="{ 
                    // 'background': 'url('+item.url+') center center no-repeat',
                    'background': 'url('+item.url+') center center no-repeat',
                    'background-size': 'auto 100%'
                }"
            ></a>
        </el-carousel-item>
      </el-carousel>
      <div class="menu-container">
        <div class="banner-menu">
            <p class="menu-title">学车流程</p>
            <ul class="menu-list">
                <li class="icon1">
                    <p class="p1"><a target="_blank" href="https://www.jiakaobaodian.com/mnks/kemu1/car.html">科目一</a></p>
                    <p class="p2">2024新题库</p>
                </li>
                <li class="icon2">
                    <p class="p1"><a target="_blank" href="https://www.jiakaobaodian.com/mnks/kemu2/car.html">科目二</a></p>
                    <p class="p2">精选视频，详解考点</p>
                </li>
                <li class="icon3">
                    <p class="p1"><a target="_blank" href="https://www.jiakaobaodian.com/mnks/kemu3/car.html">科目三</a></p>
                    <p class="p2">全方位讲解，攻克难点</p>
                </li>
                <li class="icon4">
                    <p class="p1"><a target="_blank" href="https://www.jiakaobaodian.com/mnks/kemu4/car.html">科目四</a></p>
                    <p class="p2">2024新题库</p>
                </li>
            </ul>
        </div>
      </div>


    </div>
  </template>
  
<style scoped lang="less">
.menu-container {
    position: relative;
    width: 1200px;
    height: 0;
    margin: 0 auto;
    overflow: visible;
}
.banner-menu{
    position: absolute;
    top: -358px;
    left: 0;
    width: 280px;
    z-index: 1;
    padding: 0 20px;
    background-color: rgba(255, 255, 255, .9);
    .menu-title {
        line-height: 50px;
        font-size: 20px;
        border-bottom: 1px dotted #ddd;
        text-align: center;
    }
    .menu-list {
        
        .icon1 {
            background: url(../images/km1.png) left center no-repeat;
        }
        .icon2 {
            background: url(../images/km2.png) left center no-repeat;
        }
        .icon3 {
            background: url(../images/km3.png) left center no-repeat;
        }
        .icon4 {
            background: url(../images/km4.png) left center no-repeat;
        }
        >li {
            padding: 18px 20px 18px 50px;
            .p1 {
            color: #37B5F8;
            font-size: 16px;
            }
            .p2 {
                margin-top: 5px;
                color: #666;
            }
        }
    }
}

.a-dis {
    display: inline-block;
    width: 100%;
    height: 380px;
}
</style>
<script>
export default{
    name:"Carousel",
    data(){
        return{
            imgList:[
                {
                    id:1,
                    url:new URL('../images/carouselimg1.png',import.meta.url),
                    href:"https://www.jiakaobaodian.com/download/"
                },
                {
                    id:2,
                    url:new URL('../images/carouselimg2.png',import.meta.url),
                    href:"https://www.mucang.cn/company/honor/"
                },
                {
                    id:3,
                    url:new URL('../images/carouselimg3.png',import.meta.url),
                    href:"https://www.mucang.cn/jiaolianbaodian/?from=jxrz-topbanner"
                },
                {
                    id:4,
                    url:new URL('../images/carouselimg4.png',import.meta.url),
                    href:"https://saas-shop.jiakaobaodian.com/runtu/cooperate.html"
                }
            ]
        }
        
    }
}

</script>