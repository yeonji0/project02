<template>

  <div class="row">
    <div class="visualWrap col mb-3">
        <swiper
        :navigation="true"
        :modules="modules" class="mySwiper">
          <swiper-slide v-for="(item,i) in swiperView" :key="i"
          :style="{'background-color':`${item.color}`}"
          class="p-5"
          >
              <div class="txtWrap p-5">
                  <h2 v-html="item.mainTitle"></h2>
                  <p v-html="item.subtitle" class="mb-5"></p>
              <button class="btn" >자세히보기 <span><i class="fa-solid fa-arrow-right"></i></span></button>
              </div>
              <video id="svideo" :src="`img/01mainSlide_video/${item.mVideo}`" autoplay muted loop></video>
    
          </swiper-slide>
        </swiper>
    </div>
  </div>

</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";


// import required modules
import { Navigation } from "swiper";

import sData from "@/data/01mainSlide.js"

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
      swiperView: sData,

    };
  },
};
</script>

<style lang="scss">
.visualWrap{
    width: 100%; height: 700px;
    .mySwiper{
        width: 100%;height: 100%;
        position: relative;
        #svideo{
            width: 100%;height: 100%;
            position: absolute;
            right: -20%;top: 0;

            }
        .txtWrap{
            position: absolute;
            z-index: 9999;
            color:#285E76;
            span{font-weight: bold;}
            h2{font-size: 3vw;padding: 20px 40px;}
            p{font-size: 1vw;padding: 0 40px;}
            .btn{
                margin: 0 40px;
                width: 200px; height: 60px;
                background: #fff;
                border-radius: 50px;
                box-shadow: 0 0 10px rgba(0,0,0,0.5);
                display: flex;justify-content: center; align-items: center;
                padding: 0 20px;
                span{margin-left: 20px;}
            }

        }
    }
}

</style>