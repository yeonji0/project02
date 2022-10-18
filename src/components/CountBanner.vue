<template>
  <div class="bannerWrap">
    <div class="container">
      <div class="row px-5">
        <div class="col-4 px-3">
            <img :src="`./img/banner01.jpg`" alt="" class="img-fluid rounded-5">  
        </div>
        <div class="countWrap col-8">
            <ul>
            <li>
              <div class="txtWrap">
                <span></span>
                <h4>지역네트워크</h4>
                <p>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
              </div>
              <h3>200</h3>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.bannerWrap {
  background: linear-gradient(270deg, #30cfd0 0%, #318cad 33.58%, #0b919c 100%);
  
}
.countWrap {
  display: flex;
  li {
    display: flex;
    .txtWrap {
        width: 100%;
        span{
            display: flex;
            width: 100%;height: 2px; background: red;
        }
    }
  }
}
</style>