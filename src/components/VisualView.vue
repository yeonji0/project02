<template>
  <div class="visualWrap container-fulid mb-3">
    <video id="mvideo" :src="`img/mainvideo.mp4`" autoplay muted loop></video>

    <div class="container">
      <div class="txtWrap">
        <h4>우리 청소년들이 미래의 인재로 성장하도록</h4>
        <h2>JA KOREA가 함께합니다.</h2>
        <button class="vbtn">
          자세히보기 <span><i class="fa-solid fa-arrow-right"></i></span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.visualWrap {
  display: flex;
  #mvideo {
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: relative;
    z-index: 9 !important;
  }
  .container {
    height: 100%;
    position: absolute;
    z-index: 99999;
    display: flex;
    justify-content: center;
    align-items: center;
    .txtWrap {
      color: #fff;
      h4 {
        background: #00a2ae;
        font-size: 2em;
        padding: 10px;
        @media (max-width: 991px) {
          font-size: 0.8em;
        }
      }
      h2 {
        font-weight: bold;
        font-size: 5em;
        @media (max-width: 991px) {
          font-size: 1.2em;
        }
      }
      .vbtn {
        width: 200px;
        height: 60px;
        background: #fff;
        border-radius: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 0 20px;
        span {
          margin-left: 20px;
        }
      }
    }
  }
}
</style>