<template>
  <div class="bannerWrap">
    <div class="container">
      <div class="row px-5">
        <div class="col-12 col-md-4 px-3">
          <img :src="`./img/banner01.jpg`" alt="" class="img-fluid rounded-5" />
        </div>
        <div class="countWrap col-12 col-md-8">
          <ul>
            <li>
              <div class="txtWrap">
                <span></span>
                <div class="conWrap">
                  <h4>지역네트워크</h4>
                  <p>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
                </div>
              </div>
              <h3>+200</h3>
            </li>
            <li>
              <div class="txtWrap">
                <span></span>
                <div class="conWrap">
                  <h4>학교 및 기관</h4>
                  <p>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
                </div>
              </div>
              <h3>+1,000</h3>
            </li>
            <li>
              <div class="txtWrap">
                <span></span>
                <div class="conWrap">
                  <h4>교육진행자</h4>
                  <p>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
                </div>
              </div>
              <h3>+3,000</h3>
            </li>
            <li>
              <div class="txtWrap">
                <span></span>
                <div class="conWrap">
                  <h4>교육 수혜자</h4>
                  <p>전국 17개 시도 200개이상의 지역에서 교육하고 있습니다.</p>
                </div>
              </div>
              <h3>+90,000</h3>
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
.container {
  display: flex;
  @media (max-width: 991px) {
    img {
      width: 50vw;
    }
    padding: 10px 0;
    overflow: hidden;
  }
}
.countWrap {
  @media (max-width: 991px) {
    width: 100%;
  }
  li {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    span {
      display: flex;
      width: 610px;
      height: 10px;
      background: #fff;
      border-radius: 10px;
      margin-top: 10px;
      margin-bottom: 10px;
      @media (max-width: 991px) {
        width: 200px;
        height: 5px;
      }
    }
    .txtWrap {
      width: 100%;
      color: #fff;
      .conWrap {
        display: flex;
        h4 {
          font-size: 1.2em;
          margin-right: 15px;
        }
        p {
          font-size: 1em;
        }
        @media (max-width: 991px) {
          h4 {
            font-size: 1em;
            margin-right: 0;
          }
          p {
            font-size: 1vw;
            color: #eee;
          }
        }
      }
    }
    h3 {
      font-weight: bold;
      color: #fff;
      font-size: 2em;
      @media (max-width: 991px) {
        font-size: 1em;
      }
    }
  }
}
</style>