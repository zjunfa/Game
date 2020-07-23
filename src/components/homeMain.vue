<template>
  <div class="homeMain">
    <div class="swiper-b">
      <div class="swiper">
        <el-carousel height="100%">
          <el-carousel-item v-for="(item, index) in siwperList" :key="index">
            <div class="swiper-item" :style="{'background-image': `url(${item.imgsrc})`}"></div>
          </el-carousel-item>
        </el-carousel>
      </div>
    </div>
    <div class="download">
      <div class="QRcode"></div>
      <a href="./static/down/down.html">
        <div class="QRcodetitle"></div>
        <span class="downloadbtn">点击下载</span>
      </a>
      <div class="qqQRcode"></div>
      <div class="qqQRcodetitle"></div>
      <div class="h5contact clearfix">
        <div class="quncontact fl">
          <img class="h5jiaqun" src="../assets/imgags/jiaruqqun_h5.png" />
          <ul>
            <li v-for="(item, index) in webContactList.Qqunlist" :key='index'>
              <img class="h5icon" src="../assets/imgags/qqun.png" />
              <a class="h5title" :href="item.link" target="_blank">{{item.linkname}}</a>
            </li>
          </ul>
        </div>
        <div class="qqcontact fl">
          <img class="h5jiaqq" src="../assets/imgags/lianxikefu_h5.png" />
          <ul>
            <li v-for="(item, index) in webContactList.QQlist" :key='index'>
              <img class="h5icon" src="../assets/imgags/qq.png" />
              <!-- <a class="h5title" :href="item.link" target="_blank">{{item.linkname}}</a> -->
              <a class="h5title" href="https://wpa.qq.com/msgrd?v=3&amp;uin=2868222490&amp;site=qq&amp;menu=yes" target="_blank">SKY客服1</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="contact">
      <div class="contactList">
        <img class="jiaqun" src="../assets/imgags/jiaruqqun@2x.png" />
        <ul>
          <li v-for="(item, index) in webContactList.Qqunlist" :key='index'>
            <img class="iconimg" src="../assets/imgags/qqun.png" />
            <a class="qqtitle" :href="item.link" target="_blank">{{item.linkname}}</a>
          </li>
        </ul>
        <img class="kefuimg" src="../assets/imgags/lianxikefu.png" />
        <ul>
          <li v-for="(item, index) in webContactList.QQlist" :key='index'>
            <img class="iconimg" src="../assets/imgags/qq.png" />
            <!-- <a class="qqtitle" :href='item.link' target="_blank">{{item.linkname}}</a> -->
            <a class="qqtitle" href="https://wpa.qq.com/msgrd?v=3&amp;uin=2868222490&amp;site=qq&amp;menu=yes" target="_blank">SKY客服1</a>
            <!-- https://wpa.qq.com/msgrd?v=3&amp;uin=2868222490&amp;site=qq&amp;menu=yes -->
          </li>
        </ul>
        <img class="jiaquncode" src="../assets/imgags/qqun.jpg" />
        <img class="saoma" src="../assets/imgags/saomajiaqun@2x.png" />
      </div>
    </div>
    <div class="receive" @click="receive()"></div>
    <div class="SpecialArea">
      <a class="taptap" href="https://www.taptap.com/app/191423">
        <img src="../assets/imgags/btn_041@2x.png" />
      </a>
      <a class="baidu" href="https://www.taptap.com/app/191423">
        <img src="../assets/imgags/btn_041@2x.png" />
      </a>
    </div>

  </div>
</template>

<script>
export default {
  name: 'homeMain',
  data () {
    return {
      siwperList: [
        {
          imgsrc: require('@/assets/imgags/swiper/banner_3.jpg')
        },
        {
          imgsrc: require('@/assets/imgags/swiper/banner_4.jpg')
        },
        {
          imgsrc: require('@/assets/imgags/swiper/banner_5.jpg')
        },
        {
          imgsrc: require('@/assets/imgags/swiper/banner_6.jpg')
        }
      ],
      webContactList: {
        Qqunlist: [{
          link: 'https://jq.qq.com/?_wv=1027&k=abe9BtoZ',
          linkname: '玩家交流群1'
        }],
        QQlist: [{
          link: 'https://wpa.qq.com/msgrd?v=3&amp;uin=2868222490&amp;site=qq&amp;menu=yes',
          linkname: 'SKY客服1'
        }]
      }
    }
  },
  methods: {
    receive () {
      this.$notify.closeAll()
      this.$notify({
        title: '领取规则：',
        dangerouslyUseHTMLString: true,
        message: ``,
        duration: 0
      })
    }
  },
  mounted () {

  }
}
</script>

<style scoped>
  .el-carousel {
    height: 100%;
  }

  @media screen and (min-width: 750px) {

    .homeMain {
      position: relative;
      /* min-width: 1200px; */
      /* height: 1920px; */
      width: 100vw;
      height: 100vw;
      background: url('../assets/imgags/webbg_img.jpg') no-repeat;
      background-size: 100% 100%;
    }

    .swiper {
      position: absolute;
      /* top:79px;
      left: 35px;
      width: 850px;
      height: 508px; */
      /* border-radius: 32px; */
      top: 4.11458vw;
      left: 1.822916vw;
      width: 44.27vw;
      height: 26.45vw;
      border-radius: 1.7vw;
      overflow: hidden;
    }

    .swiper-item {
      width: 100%;
      height: 100%;
      background-size: 100% 100%;
      background-position: center;
      background-repeat: no-repeat;
    }

    .swiper-b {
      /* z-index: 9; */
      position: absolute;
      /* top: 600px;
      left: 80px; */
      top: 31.25vw;
      left: 4.16vw;
      /* width: 920px;
      height: 618px; */
      width: 47.91vw;
      height: 32.18vw;
      background: url(../assets/imgags/swiper-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .download {
      position: absolute;
      /* top: 648px; */
      /* left: 1110px; */
      top: 33.75vw;
      left: 57.8125vw;
      /* width: 394px;
      height: 570px; */
      width: 20.52vw;
      height: 29.68vw;
      background: url(../assets/imgags/download-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .QRcode {
      position: absolute;
      top: 7.6vw;
      left: 50%;
      margin-left: -6.25vw;
      width: 12.5vw;
      height: 12.5vw;
      background: url(../assets/imgags/QRcode.jpg) no-repeat;
      background-size: 100% 100%;
    }

    .QRcodetitle {
      position: absolute;
      /* margin-left: 75px;
      width: 130px;
      height: 30px; */
      /* top: 400px; */
      top: 20.83vw;
      left: 50%;
      margin-left: -3.4vw;
      width: 6.77vw;
      height: 1.56vw;
      background: url(../assets/imgags/xiazai.png) no-repeat;
      background-size: 100% 100%;
    }

    .downloadbtn {
      display: inline-block;
      position: absolute;
      text-align: center;
      top: 22.83vw;
      left: 50%;
      margin-left: -3.5vw;
      width: 7vw;
      line-height: 2vw;
      background: url(../assets/imgags/button_primary.png);
      background-size: 100% 100%;
      font-size: 0.8vw;
      color: #FFFFFF;
    }

    .qqQRcode {
      display: none;
    }

    .qqQRcodetitle {
      display: none;
    }

    .h5contact {
      display: none;
    }

    .contact {
      position: absolute;
      /* top: 640px; */
      top: 33.33vw;
      right: 0;
      /* width: 288px;
      height: 1014px; */
      width: 15vw;
      height: 52.81vw;
      background: url(../assets/imgags/contact-bg.png) no-repeat;
      background-size: 100% 100%;

    }

    .contact .contactList {
      /* margin: 80px; */
      /* width: 200px; */
      margin: 4.16vw 2.6vw;
      margin-right: 0;
    }

    .contact .contactList .jiaqun {
      /* width: 114px;
      height: 33px;
      margin: 0px 0 20px; */
      width: 5.9375vw;
      height: 1.718vw;
      margin-bottom: 1.5vw;
    }

    .contact .contactList .kefuimg {
      /* width: 126px;
      height: 36px;
      margin: 30px 0 20px; */
      width: 6.5625vw;
      height: 1.875vw;
      margin: 1.5vw 0;
    }

    .contact .contactList .jiaquncode {
      /* width: 180px;
      height: 180px;
      margin: 30px 0 30px; */
      width: 9.375vw;
      height: 9.375vw;
      margin: 1.5vw 0;
    }

    .contact .contactList .saoma {
      /* width: 174px;
      height: 33px; */
      width: 9.0625vw;
      height: 1.718vw;
    }

    .contact .contactList .iconimg {
      /* width: 60px;
      height: 24px; */
      width: 3.125vw;
      height: 1.25vw;
      vertical-align: middle;
      margin-bottom: 0.3vw;
    }

    .contact .contactList .qqtitle {
      font-family: Microsoft YaHei;
      font-weight: 400;
      /* line-height:40px; */
      line-height: 2.08vw;
      color: #7E4B0E;
      /* font-size: 20px; */
      font-size: 1.04vw;
      text-decoration: underline;
    }

    .receive {
      position: absolute;
      /* top: 1298px; */
      /* left: 80px; */
      top: 67.5vw;
      left: 4.16vw;
      /* width: 620px;
      height: 354px; */
      width: 32.29vw;
      height: 18.43vw;
      background: url(../assets/imgags/receive-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .SpecialArea {
      position: absolute;
      /* top: 1298px; */
      /* left: 879.36px; */
      top: 67.5vw;
      left: 45.8vw;
      /* width: 620px;
      height: 347px; */
      width: 32.29vw;
      height: 18.07vw;
      background: url(../assets/imgags/SpecialArea-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .taptap,
    .baidu {
      display: block;
      position: absolute;
      /* top: 248px;
      left: 75px;
      width: 192px;
      height: 40px; */
      top: 12.9166vw;
      left: 3.906vw;
      width: 10vw;
      height: 2.083vw;
    }

    .baidu {
      /* left: 354px; */
      left: 18.4375vw;
    }

    .SpecialArea img {
      width: 100%;
      height: 100%;
    }
  }

  @media screen and (max-width: 750px) {
    .homeMain {
      position: relative;
      /* min-width: 320px;
      height: 2400px; */
      width: 100vw;
      height: 320vw;
      background: url('../assets/imgags/h5bg_img.jpg') no-repeat;
      background-size: 100% 100%;
    }

    .swiper {
      position: absolute;
      top: 7.2vw;
      left: 3.0666vw;
      width: 79.2vw;
      height: 47.2vw;
      border-radius: 3.2vw;
      overflow: hidden;
      /* top: 54px; */
      /* left: 23px; */
      /* width: 594px;
      height: 354px; */
    }

    .swiper-b {
      position: absolute;
      /* top: 69.86vw;
      left: 55px;
      width: 641px;
      height: 430px; */
      top: 69.86vw;
      left: 7.33vw;
      width: 85.46vw;
      height: 57.33vw;
      background: url(../assets/imgags/h5swiper-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .swiper-item {
      width: 100%;
      height: 100%;
      background-size: 100% 100%;
      background-position: center;
      background-repeat: no-repeat;
    }

    .download {
      position: absolute;
      /* top: 974px;
      left: 55px;
      width: 640px;
      height: 535px; */
      top: 129.86vw;
      left: 7.33vw;
      width: 85.33vw;
      height: 71.33vw;
      background: url(../assets/imgags/h5download-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .QRcode {
      position: absolute;
      /* top: 60px;
      left: 104px;
      width: 140px;
      height: 140px; */
      top: 8vw;
      left: 13.866vw;
      margin-left: 0;
      width: 18.666vw;
      height: 18.666vw;
      background: url(../assets/imgags/QRcode.jpg) no-repeat;
      background-size: 100% 100%;
    }

    .QRcodetitle {
      display: none;
      /* position: absolute; */
      /* top: 213px;
      left: 109px;
      width: 130px;
      height: 30px; */
      /* top: 28.4vw;
      left: 14.533vw;
      margin-left: 0;
      width: 17.333vw;
      height: 4vw;
      background: url(../assets/imgags/xiazai.png) no-repeat;
      background-size: 100% 100%; */
    }

    .downloadbtn {
      display: inline-block;
      position: absolute;
      text-align: center;
      line-height: 4.5vw;
      background: url(../assets/imgags/button_primary.png) no-repeat;
      background-size: 100% 100%;
      font-size: 2.1333vw;
      color: #FFFFFF;
      top: 28.4vw;
      left: 14.533vw;
      margin-left: 0;
      width: 17.333vw;
    }

    .qqQRcode {
      display: block;
      position: absolute;
      /* top: 60px;
      left: 104px;
      width: 140px;
      height: 140px; */
      top: 8vw;
      right: 13.866vw;
      width: 18.666vw;
      height: 18.666vw;
      background: url(../assets/imgags/qqun.jpg) no-repeat;
      background-size: 100% 100%;
    }

    .qqQRcodetitle {
      display: block;
      position: absolute;
      /* top: 213px;
      left: 109px;
      width: 130px;
      height: 30px; */
      top: 28.4vw;
      right: 14.533vw;
      width: 18.666vw;
      height: 4vw;
      background: url(../assets/imgags/saomajiaqqun_h5.png) no-repeat;
      background-size: 100% 100%;
    }

    .h5contact {
      display: block;
      position: absolute;
      /* top: 277px;
      margin-left:104px; */
      top: 36.933vw;
      margin-left: 13.8666vw;
    }

    .quncontact {
      /* width: 283px; */
      width: 37.7333vw;
    }

    .h5jiaqun,
    .h5jiaqq {
      /* height: 28px; */
      height: 3.7333vw;
    }

    .h5icon {
      /* width: 60px; */
      /* height: 24px; */
      height: 3.2vw;
      vertical-align: middle;
      /* margin-bottom: 7px; */
      margin-bottom: 0.9333vw;
    }

    .h5title {
      font-family: Microsoft YaHei;
      font-weight: 400;
      /* line-height:40px; */
      line-height: 5.3333vw;
      color: #7E4B0E;
      /* font-size: 20px; */
      font-size: 2.6666vw;
      text-decoration: underline;
    }

    .contact {
      display: none;
    }

    .receive {
      position: absolute;
      /* top: 1522px;
      left: 55px;
      width: 640px;
      height: 366px; */
      top: 202.93vw;
      left: 7.33vw;
      width: 85.33vw;
      height: 48.8vw;
      background: url(../assets/imgags/h5receive-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .SpecialArea {
      position: absolute;
      /* top: 1908px;
      left: 55px;
      width: 640px;
      height: 360px; */
      top: 254.4vw;
      left: 7.33vw;
      width: 85.33vw;
      height: 48vw;
      background: url(../assets/imgags/h5SpecialArea-bg.png) no-repeat;
      background-size: 100% 100%;
    }

    .taptap,
    .baidu {
      display: block;
      position: absolute;
      /* top: 257px;
      left: 75px;
      width: 192px;
      height: 40px; */
      top: 34.2666vw;
      left: 10vw;
      width: 25.6vw;
      height: 5.3333vw;
    }

    .baidu {
      /* left: 365px; */
      left: 48.6667vw;
    }
    .SpecialArea img {
      width: 100%;
      height: 100%;
    }
  }
</style>
<style>
  @media screen and (min-width: 750px) {
    .el-carousel__button {
        width: 0.8vw !important;
        height: 0.8vw !important;
        border-radius: 50% !important;
    }
  }
  @media screen and (max-width: 750px) {
    .el-carousel__button {
        width: 2vw !important;
        height: 2vw !important;
        border-radius: 50% !important;
    }
  }
  .el-notification{
    width: 197px !important;
    height: 285px !important;
    background: url(../assets/imgags/download-bg.png) !important;
    background-color: transparent !important;
    background-size: 100% 100% !important;
    background-position: center !important;
    background-repeat: no-repeat !important;
    border: 0px !important;
  }
  .el-notification__closeBtn {
      position: absolute;
      top: 13px !important;
      right: 23px !important;
      cursor: pointer;
      color: #909399;
      font-size: 18px;
  }
</style>
