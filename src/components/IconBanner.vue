<template>
  <div class="container mb-5">
    <div class="row  px-3 px-md-0">
        <div class="col-6 col-md bnWrap  d-md-block"
        v-for="(item,i) in ibData" :key="i" :class="{'d-none':i==4}">
        <img :src="`./img/02iconBanner/${item.src}`" alt="" class="h-50 w-50 d-block m-auto">
        <h3 v-html="item.title" class="text-center d-flex justify-content-center align-items-center" style="height:50px"></h3>
        <p v-html="item.subtitle" class="text-center px-3  d-flex justify-content-center align-items-center" style="height:50px"></p>
        </div>
    </div>
    
  </div>
</template>

<script>
export default {
    props:["ibData"],
};
</script>

<style lang="scss" scoped>
.bnWrap{
        display: flex; flex-direction: column;
        justify-content: center; align-items: center;
        h3{font-size: 1.5em; font-weight: bold;}
        p{font-size: 1em;}
        img{
            cursor: pointer;
            transition: .3s;
            &:hover{
                transform: translateY(-10px);
            }
        }
}


</style>