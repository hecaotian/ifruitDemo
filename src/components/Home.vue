<template>
  <div class="content my_swiper" id="info">
    <swiper :options="swiperOption" class="slice_main">
      <swiper-slide>
        <div class="index index1"><!--轮播图-->
          <div class="info">
            <h3>{{infotitle1}}</h3>
            <em>{{infocode1}}</em>
            <h6>{{infotext1}}</h6>
          </div>
          <div class="home_bg"></div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="index index2">
          <div class="info">
            <h3>{{infotitle2}}</h3>
            <em>{{infocode2}}</em>
            <h6>{{infotext2}}</h6>
          </div>
          <div class="home_bg"></div>
        </div>
      </swiper-slide>
      <swiper-slide>
        <div class="index index3">
          <div class="info">
            <h3>{{infotitle3}}</h3>
            <em>{{infocode3}}</em>
            <h6>{{infotext3}}</h6>
          </div>
          <div class="home_bg"></div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" id="focus" slot="pagination"></div>
      <!--<div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div>-->
    </swiper>
    <MFooter></MFooter>
  </div>
</template>
<script>
  import MFooter from '../base/MFooter';

  export default {
    name: 'Home',
    data() {
      return {
        infotitle1: '产地直供，健康原生态',
        infocode1: 'i-e亩田',
        infotext1: '坚持原产地，原生态，零农药，尊重食物本身的味道',
        infotitle2: '资本有道 兴邦有责',
        infocode2: 'VALUE VIEW',
        infotext2: '让农民有更多的希望，不忘初心，为您和您的家人提供健康的好产品是我们的责任与担当',
        infotitle3: 'i-e亩田与您同心同行 ',
        infocode3: 'COOPERATIVE',
        infotext3: 'i-e亩田以合作伙伴的关系定义企业与员工，相信相同的价值观可以促进彼此共同前行',
        swiperOption: {
          slidesPerView: 1,
          spaceBetween: 0,
          loop: true,
          autoplay: {
            delay: 5000,
            disableOnInteraction: false,
          },
          pagination: {
            el: '.swiper-pagination',
            clickable: true,

          },
          navigation: {
            nextEl: '.swiper-button-next',
            prevEl: '.swiper-button-prev'
          }
        },
      }
    },
    components: {MFooter}
  }
</script>
<style scoped lang="less">
  .content {
    height: 100%;
    width: 100%;
    overflow: hidden;
    /*轮播图*/
    .slice_main {
      height: 100%;
      width: 100%;
      overflow: hidden;
    }
    .index {
      position: relative;
      width: 100%;
      height: 100%;
      .home_bg {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background: url("../image/bg-dot.png");
      }

    }
    .index1 {
      background: url('../image/indexpic01.jpg') center center no-repeat;
      background-size: cover;
    }
    .index2 {
      background: url('../image/indexpic02.jpg') center center no-repeat;
      background-size: cover;
    }
    .index3 {
      background: url('../image/indexpic03.jpg') center center no-repeat;
      background-size: cover;
    }
    /*中间内容区*/
    .info {
      position: absolute;
      top: 30%;
      width: 100%;
      color: #fff;
      z-index: 100;
      text-align: center;
      h3 {
        font-size: 26px;
      }
      em {
        display: inline-block;
        font-size: 34px;
        color: #45caff;
        margin-top: 25px;
        font-family: 'Helvetica Neue';
        font-style: normal;
        font-weight: bold;
        border-bottom: 1px solid #45caff;
      }
      h6 {
        margin: 30px auto;
        width: 57%;
        height: 25px;
        font-weight: normal;
        line-height: 35px;
        font-size: 20px;
      }
    }
  }

  /*适配*/
  /*轮播图区*/
  @media all and(max-width: 760px) {
    #info {
      #focus {
        bottom: 105px;

      }
      .info {
        top: 28%;
        h3 {
          font-size: 24px;
        }
        em {
          font-size: 32px;
        }
        h6 {
          width: 70%;
          font-size: 18px;

        }
      }
    }
  }

  @media all and(max-width: 500px) {
    #info {
      #focus {
        bottom: 95px;

      }
      .info {
        top: 25%;
        h3 {
          font-size: 22px;
        }
        em {
          font-size: 32px;
        }
        h6 {
          width: 75%;
          font-size: 16px;

        }
      }
    }
  }

  @media all and(max-width: 375px) {
    #info {
      #focus {
        bottom: 85px;
      }
      .info {
        top: 20%;
        h3 {
          font-size: 20px;
        }
        em {
          font-size: 28px;
        }
        h6 {
          width: 80%;
          font-size: 14px;

        }
      }
    }
  }

</style>
