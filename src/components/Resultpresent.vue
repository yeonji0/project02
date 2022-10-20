<template>
  <div class="container p-3" v-for="(item,i) in 4" :key="i">
    <div class="contents">
       
            <h4>
                {{result[i].title}}
             </h4>
  
        <div class="txtWrap">
            <p>{{result[i].date}}</p>
        </div>
        <span></span>
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
  border-radius: 20px; transition: .5s;
  &:hover{box-shadow: 0 0 10px rgba(0,0,0,0.5);}
  .contents{
     display: flex; flex-direction: column;
     position: relative;
          span{
        width: 100%;height: 2px;background: #eee;
        position: absolute;
        bottom: -17px;
        }
    h4{
         font-size: 1em;
          font-weight: bold;
    }
  }
}
</style>