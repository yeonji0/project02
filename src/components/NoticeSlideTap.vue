<template>
  <div class="tapWrap">
    <swiper
      v-bind="swiperOptions1"
      :modules="modules1"
      class="mySwiper1 p-5">
        <swiper-slide v-if="tab==1" v-for="item in notice" :key="item" class="slide p-5" :class="{notice:tab=1}">
          <h4>{{item.name}}</h4>
          <div class="title">{{item.title}}</div>
          <p v-html="item.content"></p>
        </swiper-slide>
        <swiper-slide v-if="tab==2" v-for="item in story" :key="item" class="slide p-5" :class="{notice:tab=2}">
          <h4>{{item.name}}</h4>
           <div class="title">{{item.title}}</div>
           <p v-html="item.subtitle"></p>
        </swiper-slide>
        <swiper-slide v-if="tab==3" v-for="item in news" :key="item" class="slide p-5" :class="{notice:tab=3}">
          <h4>{{item.name}}</h4>
           <div class="title">{{item.title}}</div>
           <p v-html="item.content"></p>
        </swiper-slide>
      </swiper>
      <div class="btnWrap">
        <div class="prev"><img :src="`./img/prev.png`" alt=""></div>
        <div class="next"><img :src="`./img/next.png`" alt=""></div>
      </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Pagination,Navigation } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  props:[
    "notice",
    "story",
    "news",
    "tab"
  ],
  setup() {
    return {
      modules1: [Navigation,Pagination],
      swiperOptions1:{
        breakpoints:{
          1200: {
            slidesPerView:3,
          },
          900: {
            slidesPerView:2,
          }
        },
        spaceBetween:30,
        loop:true,
        observer: true,
        observeParents: true,
         navigation:{
          nextEl:'.tapWrap .next',
          prevEl:'.tapWrap .prev',
        },
      }
    };
  },
};
</script>

<style lang="scss" scoped>
.tapWrap{
  position: relative;
  .btnWrap{
    width: 100%;
    position: absolute;
    display: flex; justify-content: space-between;
    top: 50%;
    z-index: 100;
    .next, .prev{
      width: 70px;height: 50px;
      display: flex;justify-content: center;align-items: center;
      background: #fff; border-radius: 30px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
      cursor: pointer;
      }
  }

}
.mySwiper1{
  height: 500px;
.slide{
    width: 100px; height: 100%;
    h4{
        background: #000; color: #fff;
        width: 80px;height: 30px;
        font-size: 0.7vw;
        display: flex; justify-content: center;align-items: center;
        border-radius: 50px;
    }
    .title{
      font-weight: bold; font-size: 1.3vw;
      height: 80px;
      overflow: hidden;
      text-overflow: hidden;
      }
    p{text-overflow: hidden; height: 93px; overflow: hidden;}
    }
}

</style>