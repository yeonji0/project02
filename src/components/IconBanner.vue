<template>
  <div class="container mb-5">
    <div class="row">
        <div class="col-6 col-lg bnWrap"
        v-for="(item,i) in ibData" :key="i">
        <img :src="`./img/02iconBanner/${item.src}`" alt="" class="w-50 h-50">
        <h3 v-html="item.title" class="text-center"></h3>
        <p v-html="item.subtitle" class="text-center"></p>
        </div>
    </div>
    
  </div>
</template>

<script>
export default {
    props:["ibData"],
};
</script>

<style lang="scss">
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