<template>
  <div class="container">
    <div class="row">
      <div class="txtWrap col-lg-4 mb-3">
        <h4>국내외 여러기업이 동참하고 있습니다.</h4>
        <h2 class="mb-5">JA Korea 후원</h2>
        <button class="btn">
            자세히보기 <span><i class="fa-solid fa-arrow-right"></i></span>
        </button>
      </div>
      <support-slide class="col-lg-8" :supot="supot"></support-slide>
    </div>
  </div>
</template>
<script>
// Import Swiper Vue.js components
import SupportSlide from "@/components/SupportSlide.vue"

export default {
  components:{SupportSlide},
  props:[
    "supot"
  ],
};
</script>


<style lang="scss" scoped>
.container{
  .txtWrap{
    display: flex;justify-content: center;
    flex-direction: column;
    
    h4{ color: #00a2ae;
        font-size: 1em;
        font-weight: bold;
        @media (max-width: 991px) {
          font-size: 0.7em;
        }

      }
    h2 {
        font-weight: bold;
        font-size: 3em;
        @media (max-width: 991px) {
          font-size: 2em;
        }
      }
      .btn {
          width: 200px;
          height: 60px;
          background: #fff;
          border-radius: 50px;
          display: flex;
          justify-content: center;
          align-items: center;
          padding: 0 20px;
          box-shadow: 0 0 10px rgba(0,0,0,0.3);
          span {
            margin-left: 20px;
          }
          @media (max-width: 991px) {
            width: 150px;
            height: 50px;
            padding: 0;
        }
        }
  }

}

</style>