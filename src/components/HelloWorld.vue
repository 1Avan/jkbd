<template>
  <div>
    <!-- 顶部区域 -->
    <header class="header">
      <div class="header-top">
        <!-- logo区域 -->
        <div class="logo-w" >
          <a class="logo" href="https://www.jiakaobaodian.com/"></a>
        </div>
        <!-- 搜索框 -->
        <div class="search-w">
          <form action="https://www.so.com/s" target="_blank" id="so360form">
            <input type="text" placeholder="请输入关键字" autocomplete="off" name="q" id="so360_keyword" class="search-input">
            <input type="submit" class="button" ref="soSubmit" id="so360_submit" value="搜 索">
            <input type="hidden" name="ie" value="utf8"><input type="hidden" name="src" value="zz_jiakaobaodian.com"><input type="hidden" name="site" value="jiakaobaodian.com">
            <input type="hidden" name="rg" value="1">
          </form>
        </div>
      </div>
          <!-- 导航栏 -->
      <nav class="horizontal-nav">
        <ul class="nav-w">
          <li><a @click="selectNavItem('home')" :class="{ 'active': selectedNavItem === 'home' }" href="https://www.jiakaobaodian.com/" >首页</a></li>
          <li class="menu-jx" @click="selectNavItem('mnks')">
            <a class="" href="https://www.jiakaobaodian.com/mnks/" :class="{ 'active': selectedNavItem === 'mnks' }">模拟考试</a>
            <div class="drop-w">
              <a href="https://www.jiakaobaodian.com/mnks/kemu1/car.html">科目一</a>
              <a href="https://www.jiakaobaodian.com/mnks/kemu2/car.html">科目二</a>
              <a href="https://www.jiakaobaodian.com/mnks/kemu3/car.html">科目三</a>
              <a href="https://www.jiakaobaodian.com/mnks/kemu4/car.html">科目四</a>
            </div>
          </li>
          <li class="menu-jx" @click="selectNavItem('school')" >
            <a  href="https://www.jiakaobaodian.com/school/" :class="{ 'active': selectedNavItem === 'school' }">找驾校</a>
            <div class="drop-w">
              <a href="https://www.jiakaobaodian.com/school/">找驾校</a>
              <a href="https://www.jiakaobaodian.com/coach/">找教练</a>
              <a href="https://www.jiakaobaodian.com/peilian/">找陪练</a>
            </div>
          </li>
          <li><a class="" href="https://www.jiakaobaodian.com/bbs/" @click="selectNavItem('bbs')" :class="{ 'active': selectedNavItem === 'bbs' }">驾考圈</a></li>
          <li><a class="" href="https://www.jiakaobaodian.com/sign/" @click="selectNavItem('sign')" :class="{ 'active': selectedNavItem === 'sign' }">交通标志</a></li>
          <li><a class="" href="https://www.jiakaobaodian.com/download/" @click="selectNavItem('download')" :class="{ 'active': selectedNavItem === 'download' }">软件下载</a></li>
          <li class="qiye"><a href="https://qiye.jiakaobaodian.com" target="_blank" rel="nofollow">驾考宝典企业版</a></li>
          <li><a href="https://www.futurephantom.cn/" target="_blank" rel="nofollow">智慧驾校</a></li>
          <li class="menu-jx"><a href="https://www.maiche.com/rank/?from=jiakao_web" >买新车</a><div class="drop-w"><a href="https://www.maiche.com/rank/?from=jiakao_web" target="_blank" rel="nofollow">买车网</a><a href="http://www.pingxing.cn" target="_blank" rel="nofollow">平行之家</a></div></li>
          <li><a href="http://www.xiaozhu2.com/?from=jiakao_web" target="_blank" rel="nofollow">二手车</a></li>
        </ul>
      </nav>

    </header>


    <!-- 轮播图 -->
    <div class="carousel">
      <Carousel/>
    </div>
  </div>
</template>

<script>
// 导入轮播图组件
import Carousel from './Carousel.vue';
export default {
  components:{
    Carousel,
  },
  name: 'HelloWorld',
  data(){
    return{
      selectedNavItem:""
    }
  },
  methods:{
    selectNavItem(item) {
      this.selectedNavItem = item;
    }
  }
  
}
</script>

<style scoped lang="less">

header {
  height: 148px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  
}
header .header-top{
  width: 1200px;
  height: 42px;
  margin: 28px auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .logo-w{
    width: 207px;
    height: 100%;
    overflow: hidden;
    font-size: 36px;
    .logo{
      display: block;
      width: 207px;
      height: 100%;
      background: url(../images/logo.png) left center no-repeat;
    }
  }

    .search-w{
      position: relative;
      width: 300px;
      input{
      float: left;
      height: 42px;
      width: 100%;
      line-height: 40px;
      border: 1px solid #e9e9e9;
      font-size: 14px;
      padding: 0 40px 0 10px;
      }
      
      .button {
        position: absolute !important;
        top: 0 !important;
        right: 0 !important;
        width: 14% !important;
      }

  }

    input:focus {
    outline: none; 
    border:1px solid #007aff; /* 输入框获得焦点时的边框颜色 */
  }

}

.horizontal-nav{
  width: 100%;
  height: 50px;
  background-color: #37B5F8;
  color: #fff;
  .nav-w{
    width: 1200px;
    margin: auto;
    height: 50px;
    line-height: 50px;
    font-size: 16px;
    text-align: left;
    .qiye {
      width: 148px;
    }
    .menu-jx {
      position: relative;
      overflow: visible;
 
      >a:after{
        display: inline-block;
        vertical-align: middle;
        width: 10px;
        height: 10px;
        margin-left: 6px;
        margin-top: 5px;
        border: 5px solid transparent;
        border-top: 5px solid #fff;
        content: ' ';
      }
      .drop-w{
          font-size: 14px;
          display: none;
          position: absolute;
          top: 50px;
          width: 100%;
          background-color: #fff;
          z-index: 2;
          line-height: 40px;
          padding: 0 8px;
          color: #666;
          box-shadow: 0 0 20px rgba(0,0,0,.1);
          >a:hover {
            color: #37b5f9;
          }
      }
    }

    .menu-jx:hover .drop-w{
      display: block;
    }
    >li:hover{
      background-color:#54c0f9;
    }


    >li{
      display: inline-block;
      padding: 0;
      vertical-align: top;
      width: 108px;
      text-align: center;
      a {
        display: block;
        height: 100%;
        width: 100%;
      }

      .active {
        background-color: #258FC7;
      }
    }
  }

}


</style>
