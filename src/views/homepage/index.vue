<template>
  <div style="background:#f0f2f5;margin-top: -20px;">
    <div class="wscn-http404">
      <div class="pic-homepage">
        <img class="pic-homepage-map" :src="mapPic" alt="map">
        <!-- <img class="pic-404__child left" :src="img_404_cloud" alt="404">
        <img class="pic-404__child mid" :src="img_404_cloud" alt="404">
        <img class="pic-404__child right" :src="img_404_cloud" alt="404"> -->
      </div>
      <!-- <div class="bullshit">
        <div class="bullshit__oops">OOPS!</div>
        <div class="bullshit__info">版权所有<a class='link-type' href='https://wallstreetcn.com' target='_blank'>华尔街见闻</a></div>
        <div class="bullshit__headline">{{ message }}</div>
        <div class="bullshit__info">请检查您输入的网址是否正确，请点击以下按钮返回主页或者发送错误报告</div>
        <a href="/" class="bullshit__return-home">返回首页</a>
      </div> -->
    </div>
  </div>
</template>

<script>
import mapPic from '@/assets/homepage_images/map.png'
// import img_404_cloud from '@/assets/404_images/404_cloud.png'

export default {
  data() {
    return {
      mapPic
    //   img_404_cloud
    }
  }
//   computed: {
//     message() {
//       return '特朗普说这个页面你不能进......'
//     }
//   }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.wscn-http404 {
  position: relative;
  width: 100%;
  margin: 20px auto 60px;
  padding: 0 36px;
  overflow: hidden;
  .pic-homepage {
    position: relative;
    float: left;
    width: 100%;
    padding: 0 0;
    overflow: hidden;
    &__map {
      width: 100%;
    }
    // @keyframes cloudMid {
    //     0% {
    //       top: 10px;
    //       left: 420px;
    //       opacity: 0;
    //     }
    //     20% {
    //       top: 40px;
    //       left: 360px;
    //       opacity: 1;
    //     }
    //     70% {
    //       top: 130px;
    //       left: 180px;
    //       opacity: 1;
    //     }
    //     100% {
    //       top: 160px;
    //       left: 120px;
    //       opacity: 0;
    //     }
    // }
  }
}
</style>
