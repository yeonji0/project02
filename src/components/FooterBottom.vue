<template>
    <div class="container">
        <div class="ftbottom">
                    <ul>
                        <li><a href="#!">후원하기</a></li>
                        <li><a href="#!">온라인 학습관리</a></li>
                        <li><a href="#!">기금영수증</a></li>
                        <li><a href="#!">국세청 공시 및 공개 내역</a></li>
                        <li><a href="#!">1:1 문의</a></li>
                    </ul>
                    <div class="footer py-3">
                        <h1><img :src="`./img/footer-logo.png`" alt=""></h1>
                        <p>서울특별시 강서구 양천로 583, B동 1408호(염창동, 우림블루나인비즈니스센터) 사단법인 제이에이코리아    우편번호 : 07547    대표 : 이은형    사업자번호 : 107-82-10367</p>
                        <p>대표전화 : 02-783-2367    팩스 : 070-4275-5115    이메일 : jakorea@jakorea.org</p>
                        <p>ⓒJA Korea,2022</p>
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
    .ftbottom{
        height: 100%;
        ul{
            height: 100%;
            display: flex; align-items: center;
            a{
                padding: 10px;
                display: flex;
                color: #aaa;
            }
        }
        .footer{
            color: #aaa;
        }
    }
}
</style>