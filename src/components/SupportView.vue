<template>
  <div class="container">
    <div class="row">
      <div class="txtWrap col-4">
        <h2>국내외 여러기업이 동참하고 있습니다.</h2>
        <h2>JA Korea 후원</h2>
        <button class="vbtn">
            자세히보기 <span><i class="fa-solid fa-arrow-right"></i></span>
        </button>
      </div>
      <support-slide class="col-8"></support-slide>
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

</style>