<template>
  <div class="container p-3" v-for="(item,i) in 4" :key="i">
    <div class="name">
        <h4 :class="{ing:post[i].name == '모집중'}">
            {{ post[i].name }}
         </h4>
    </div>
    <div class="txtWrap">
      <h3>{{ post[i].title }}</h3>
      <p>{{ post[i].operate }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["post"],
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  border-radius: 20px; transition: .5s;
  &:hover{box-shadow: 0 0 10px rgba(0,0,0,0.5);}
  
  .name{

    margin-right: 15px;
      h4 {
        background: #318cad;
        color: #fff;
        width: 80px;
        height: 30px;
        font-size: 0.7vw;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50px;
        &.ing{
            background: #000;
        }
      }
  }
  .txtWrap {
    display: flex;
    flex-direction: column;
    h3 {
      font-size: 1em;
      font-weight: bold;
    }
  }
}
</style>