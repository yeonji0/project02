<template>
  <div class="container_w">
    <div class="visualWrap col mb-3">
      <swiper
        v-bind="swiperOptions"
        :navigation="true"
        :pagination="true"
        :modules="modules"
        class="mySwiper"
      >
        <swiper-slide
          v-for="(item, i) in swiperView"
          :key="i"
          :style="{ 'background-color': `${item.color}` }"
        >
          <div class="txtWrap">
            <h2 v-html="item.mainTitle"></h2>
            <p v-html="item.subtitle" class="mb-5"></p>
            <button class="btn">
              자세히보기 <span><i class="fa-solid fa-arrow-right"></i></span>
            </button>
          </div>
          <video
            id="svideo"
            :src="`img/01mainSlide_video/${item.mVideo}`"
            autoplay
            muted
            loop
          ></video>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

// import required modules
import { Navigation, Pagination, Mousewheel, Keyboard } from "swiper";

import sData from "@/data/01mainSlide.js";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation, Pagination, Mousewheel, Keyboard],
      swiperView: sData,
      swiperOptions: {
        loop: true,
      },
    };
  },
};
</script>

<style lang="scss">
.visualWrap {
  width: 100%;
  height: 700px;
  @media (max-width: 991px) {
  height: 700px;}
  .mySwiper {
    width: 100%;
    height: 100%;
    position: relative;

    #svideo {
      width: 100%;
      height: 100%;
      position: absolute;
      right: -20%;
      top: 0;
    }
    @media (max-width: 991px) {
      #svideo { 
        right: -20px;
        top: 100px;
      }
      .swiper-slide{overflow: hidden;}
    }
    .txtWrap {
      position: absolute;
      z-index: 9999;
      color: #285e76;
      top: 50%;
      transform: translateY(-50%);
      left: calc( 50% - 600px );
      span {
        font-weight: bold;
      }
   
      }

      @media (max-width: 991px) {
        .txtWrap{
          top: 20px; left: 20px;
          transform: initial;
        } 


      h2 {
        font-size: 3vw;
        padding: 20px 40px;
      }
      p {
        font-size: 1vw;
        padding: 0 40px;
      }
      .btn {
        margin: 0 40px;
        width: 200px;
        height: 60px;
        background: #fff;
        border-radius: 50px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 20px;
        span {
          margin-left: 20px;
        }
      }
    }
  }
  .btnWrap {
    display: block;
    position: absolute;
    bottom: 0;
  }
}

</style>