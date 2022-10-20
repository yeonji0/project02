<template>
  <div class="resultWrap">
    <div class="container">
      <div class="row">
        <div class="post col-lg-6">
          <h4 class="mb-3">모집공고<span></span></h4>
          <result-post :post="post"></result-post>
        </div>
        <div class="result col-lg-6">
          <h4 class="mb-3">결과발표<span></span></h4>
          <resultpresent :result="result"></resultpresent>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ResultPost from "@/components/ResultPost.vue";
import Resultpresent from "@/components/Resultpresent.vue";

export default {
  components: {
    ResultPost,
    Resultpresent,
  },
  props: ["post", "result"],
};
</script>

<style lang="scss" scoped>
.container {
  h4 {
    font-weight: bold;
    font-size: 2em;
  }
  span {
    display: flex;
    width: 100%;
    height: 3px;
    background: #333;
    margin: 10px 0;
  }
}
</style>