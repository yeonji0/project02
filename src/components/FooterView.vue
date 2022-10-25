<template>
 <div class="container-fluid">
    <div class="container">
        <div class="row">
            <div class="ftTop">
                <ul>
                    <li><a href="#!">이용약관</a></li>
                    <li><a href="#!" class="active">개인정보처리방침</a></li>
                    <li><a href="#!">이메일수집거부</a></li>
                    <li><a href="#!">오시는길</a></li>
                </ul>
            </div>
           
        </div>
    </div>

</div>
  

</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.container-fluid{
    background: #F6F6F6;
    .ftTop{
        height: 80px;
        display: flex;justify-content: start;
        ul{
            height: 100%;
            display: flex; align-items: center;
            a{
                font-weight: bold;
                padding: 20px;
                &.active{color: #285F74;}
            }
        }
    }
}
</style>