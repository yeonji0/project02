<template>
<div class="slideWrap">
    <div class="container">
        <div class="menuWrap">
            <h1>JA 기관소식</h1>
            <div class="row tabMenu">
                <div class="col tab" @click="tab=1" :class="{active:tab==1}">공지사항<span></span></div>
                <div class="col tab" @click="tab=2" :class="{active:tab==2}">스토리<span></span></div>
                <div class="col tab" @click="tab=3" :class="{active:tab==3}">언론보도<span></span></div>
            </div>
        </div>
        <notice-slide-tap :notice="notice" :story="story" :news="news" :tab="tab"></notice-slide-tap>
    </div>
</div>
</template>

<script>
import NoticeSlideTap from "@/components/NoticeSlideTap.vue"

export default {
    components:{NoticeSlideTap},
    props:[
        "notice",
        "story",
        "news",
        "tab"
    ],
    data(){
        return{
            tab:1,
            
        }
    }

}
</script>

<style lang="scss" scoped>
.container{
    .menuWrap{
        font-weight: bold;
        h1{width: 300px; font-weight: bold;}
        display: flex;
        @media (max-width: 991px) {flex-direction: column;}
        .tabMenu{
            width: 100%;
            display: flex;
            font-size: 1.3em;
            div{
                width: 100%;
                display: flex;justify-content: center;align-items: center;
                cursor: pointer;
                position: relative;
                span{
                width: 70%; height: 5px; position: absolute;
                bottom: 10%;background:  #365A66;
                display: none;
                }
                &.active{
                    span{display: block;}
                }
            }

        }
    }
    .notice-slide-tap{height: 100%;}
}

</style>