<template>
  <div class="container" v-for="(item,i) in 4" :key="i">
    <div class="name">
        <h4>
            {{result[i].title}}
         </h4>
    </div>
    <div class="txtWrap">
    </div>
  </div>
</template>

<script>
export default {
    props:["result"],


}
</script>

<style lang="scss" scoped>
.container {
  display: flex;
 
}
</style>