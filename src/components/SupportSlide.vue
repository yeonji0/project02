<template>
    <div class="slideWrap">
      <swiper
         :modules="modules2"
          v-bind="swiperOptions2" 
          class="mySwiper02">
          
        <swiper-slide v-for="item in supot" :key="item">
          <img :src="`./img/09support/${item.src}`" alt="">
        </swiper-slide>
      </swiper>
      <div class="btnWrap">
        <div class="prev"><img :src="`./img/prev_gr.png`" alt=""></div>
        <div class="next"><img :src="`./img/next_gr.png`" alt=""></div>
      </div>
    </div>
  </template>
  <script>
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from "swiper/vue";
  
  // Import Swiper styles
  import "swiper/css";
  
  import "swiper/css/grid";
  import "swiper/css/navigation";
  
  
  // import required modules
  import { Grid,Navigation } from "swiper";
  
  export default {
    props:[
      "supot"
    ],
    components: {
      Swiper,
      SwiperSlide, 
    },
    setup() {
      return {
        modules2: [Grid,Navigation],
        swiperOptions2:{
          slidesPerView:3,
          grid:{
              rows: 3,
            },
          spaceBetween:10,
          pagination:{
              clickable: true,
            },
        navigation:{
          nextEl:'.next',
          prevEl:'.prev',
        },  
        }
      };
      
    },
  };
  </script>

<style lang="scss" scoped>
.slideWrap{
  height: 500px;
  position: relative;
  .swiper {
  width: 100%;
  height: 100%;
  margin-left: auto;
  margin-right: auto;
}

.swiper-slide {
  background: #fff;
  height: calc((100% - 120px) / 3) !important;
  background: #eee;
  padding: 40px;
  border-radius: 10px;
  img{width: 100%;height: 100%;}
  }

  .btnWrap{
    width: 100%;
    position: absolute;
    display: flex;
    left: -50%;bottom:20%;
    gap: 50px;
    z-index:1000;
    .next, .prev{
      width: 70px; height: 100%;
      padding: 10px;
      cursor: pointer;
    }

  }
}

</style>