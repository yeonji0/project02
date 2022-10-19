<template>
  <div class="container mb-5">
   
    <div class="eduWrap">
      <h1>JA 교육 프로그램</h1>
      <div class="menuWrap">
          <ul>
            <li>진로취업</li>
            <li>경제금융</li>
            <li>기업가정신</li>
            <li>디지털 리터러시</li>
          </ul>
      </div>
    </div>
    <span class="bg"></span>

    <swiper 
    :navigation="true" 
    :modules="modules" class="mySwiper">

      <swiper-slide v-for="(item,i) in eduData" :key="i" class="slide p-5">
        <div class="txtWrap p-5">
            <h2 v-html="item.name" ></h2>
            <h2 v-html="item.title" class="mb-3"></h2>
            <p v-html="item.subtitle" class="mb-5"></p>
            <button class="btn" >자세히보기 <span><i class="fa-solid fa-arrow-right"></i></span></button>
        </div>
        <div class="imgWrap">
            <img :src="`./img/03eduProgram/${item.src}`" alt="" class="img-fluid">
        </div>
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
.container{
  position: relative;
  padding: 50px 0;
  }
.bg{
  display: block; width: 500px;height: 120%;background: #eee;
  border-radius: 30px;
  position: absolute;
  top: -15%;right: -20%; 
}
.eduWrap {
  display: flex;
  gap:50px;
  font-weight: bold;
 
  .menuWrap{
    
    ul{display: flex; padding: 0;height: 100%;}
    li{
        height: 100%; display: flex; justify-content: center; align-items: center;
        display: flex; padding:0 20px;
    }
    
  }
}
.mySwiper {
  height: 500px;
  display: flex;
  h2{font-weight: bold;}
  .slide{display: flex; gap:50px;}
  .imgWrap{
    img{width: 100%;height: 100%;}
  }

}
.txtWrap{
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


/********** css responsive **********/
@media (max-width: 1399px) {
    
}

@media (max-width: 1199px) {
    
}

@media (max-width: 991px) {
    .bg{display: none;}
    .eduWrap{
      flex-direction: column;
      gap: 10px;
      h1{padding: 0 10px;}
      .menuWrap{
        li{padding: 0 10px;}
      }
    }
}

@media (max-width: 767px) {
    
}

@media (max-width: 575px) {
    
}
</style>