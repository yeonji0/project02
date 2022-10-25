<template>

  
    <div class="visualWrap mb-3">
      <video id="mvideo" :src="`img/mainvideo.mp4`" autoplay muted loop></video>
      <div class="txtWrap">
        <h4>우리 청소년들이 미래의 인재로 성장하도록</h4>
        <h2>JA KOREA가 함께합니다.</h2>
        <button class="btn">
          자세히보기 <span><i class="fa-solid fa-arrow-right"></i></span>
        </button>
      </div>

    </div>

</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.visualWrap {
  width: 100%;
  padding-top: 50%;
  position: relative;
  overflow: hidden;
  #mvideo {
    position: absolute;
    left:50%;top: 50%;
    transform: translate(-50%,-50%);
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
    .txtWrap {
      position: absolute;
      color: #fff;
      top: 20%; left: calc(50% - 700px);
      @media (max-width: 991px) {
        left:10%;
        }
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
      }
    }
  }
</style>