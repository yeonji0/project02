<template>
  <div class="container">
    <div class="eduWrap">
      <h1>JA 교육 프로그램</h1>
      <div class="menuWrap">
          <ul>
            <li><a href="#">진로취업</a></li>
            <li><a href="#">경제금융</a></li>
            <li><a href="#">기업가정신</a></li>
            <li><a href="#">디지털 리터러시</a></li>
          </ul>
      </div>
    </div>
    <swiper 
    :navigation="true" 
    :modules="modules" class="mySwiper">
      <swiper-slide v-for="(item,i) in eduData" :key="i">
        {{item.name}}

      </swiper-slide>
    </swiper>
  </div>
</template>
<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/navigation";

// import required modules
import { Navigation } from "swiper";
import eduData from "@/data/03eduProgram.js";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Navigation],
      eduData: eduData,
    };
  },
};
</script>


<style lang="scss">
.eduWrap {
  display: flex;
  gap:50px;
  h1{font-weight: bold;}
  .menuWrap{
    ul{display: flex; padding: 0;height: 100%;}
    li{
        height: 100%; display: flex; justify-content: center; align-items: center;
        a{display: flex; padding:0 20px;}
    }
    
  }
  
}
.mySwiper {
  height: 500px;
}
</style>