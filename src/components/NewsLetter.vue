<template>
  <div class="container">
    <div class="row">
        <div class="newsWrap col-8">
            <div class="txtWrap p-5">
                <h4>JA KOREA 뉴스레터 구독하기</h4>
                <div class="inpWrap py-lg-3">
                    <div class="name">
                        <p><i class="fa-regular fa-user"></i></p>
                        <input class="inp" type="text" placeholder="이름">
                    </div>
                    <div class="adr">
                        <p><i class="fa-regular fa-envelope"></i></p>
                        <input class="inp" type="text" placeholder="이메일주소">
                    </div>
                    <button class="btn">신청하기</button>
                </div>
                <p class="agree"><i class="fa-regular fa-circle-check"></i> 뉴스레터 구독을 위한 이름 및 이메일 주소 수집에 동의합니다.</p>
            </div>
        </div>
        <div class="imgWrap col-4">
            <img :src="`img/subscribe.png`" alt="">
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.container{
    background:rgba(5, 159, 171, 1);
    border-radius: 10px;
    .newsWrap{
        @media (max-width: 991px) {padding: 0; margin: 0;}
        .txtWrap{
            color: #fff;
            line-height: 30px;
            .agree{
                @media (max-width: 991px) {width:150%;font-size:0.8em;}
            }
            h4{font-weight: bold;
            font-size: 2em;
            @media (max-width: 991px) {font-size: 1em;}
        }
            .btn{
                border: 1px solid #fff;
                color: #fff;
                padding: 10px;
                @media (max-width: 991px) {width:300px}
            }
            .inpWrap{
                display: flex; width: 100%; gap: 10px;
                @media (max-width: 991px) {flex-direction: column;}
            }
            .name, .adr{
                position: relative;
                input {
                width: 300px;
                height: 50px;
                font-size: 15px;
                border: 0;
                border-radius: 15px;
                outline: none;
                padding-left: 10px;
                background-color: rgba(255, 255, 255, 0.2);
                position: relative;
                text-indent: 30px;
                &::placeholder {color: white;}
             
                }
                p{
                    width: 100%;height: 100%;
                    position: absolute; 
                    display: flex;align-items: center;
                    padding: 0 10px;
                    
                }
            }
        }
    }
    .imgWrap{
        position: relative;
        img{position: absolute;
        top: -10%;}
        @media (max-width: 991px) {display: none;}
    }
}

</style>