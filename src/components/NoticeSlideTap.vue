<template>
  <swiper 
    v-bind="swiperOptions1"
    :modules="modules1" 
    class="mySwiper1">

      <swiper-slide v-if="tab==1" v-for="item in notice" :key="item" class="slide p-5" :class="{notice:tab=1}">
        <h4>{{item.name}}</h4>
        <div class="title">{{item.title}}</div>
        <p v-html="item.content"></p>
      </swiper-slide>

      <swiper-slide v-if="tab==2" v-for="item in story" :key="item" class="slide p-5" :class="{notice:tab=2}">
        <h4>{{item.name}}</h4>
         <div class="title">{{item.title}}</div>
      </swiper-slide>

      <swiper-slide v-if="tab==3" v-for="item in news" :key="item" class="slide p-5" :class="{notice:tab=3}">
        <h4>{{item.name}}</h4>
         <div class="title">{{item.title}}</div>
      </swiper-slide>

    </swiper>
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
        slidesPerView:3,
            spaceBetween:30,
            loop:true,
            observer: true,
            observeParents: true,
      }
    };
  },
};
</script>

<style lang="scss" scoped>
.mySwiper1{
.swiper-slide{
    width: 200px;
    h4{
        background: #000; color: #fff;
        width: 80px;height: 30px;
        font-size: 0.7vw;
        display: flex; justify-content: center;align-items: center;
        border-radius: 50px;
    }
    .title{font-weight: bold; font-size: 1.5vw;}
    }
}
</style>