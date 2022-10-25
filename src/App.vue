<template>
<header-view></header-view>
<main-visual v-bind:mslide="mslide"></main-visual>
<icon-banner :ibData="ibData"></icon-banner>
<edu-slide :eduData="eduData"></edu-slide>
<count-banner></count-banner>
<notice-slide
:notice="notice"
:story="story"
:news="news"></notice-slide>
<result-view :post="post" :result="result"></result-view>
<visual-view></visual-view>
<support-view :supot="supot"></support-view>
<news-letter></news-letter>
<footer-view></footer-view>
<footer-bottom></footer-bottom>


</template>

<script>
import "@/assets/style.css"

import headerView from "@/components/headerView.vue"

import mainVisual from "@/components/mainVisual.vue"
import mslide from "./data/01mainSlide.js"

import IconBanner from "@/components/IconBanner.vue"
import ibData from "./data/02iconBanner.js"

import EduSlide from "@/components/EduSlide.vue"
import eduData from "./data/03eduProgram.js"

import CountBanner from "@/components/CountBanner.vue"

import NoticeSlide from "@/components/NoticeSlide.vue"
import notice from "@/data/04notice.js"
import story from "@/data/05story.js"
import news from "@/data/06news.js"

import ResultView from "@/components/ResultView.vue"
import post from "@/data/07post.js"
import result from "@/data/08result.js"

import VisualView from "@/components/VisualView.vue"

import SupportView from "@/components/SupportView.vue"
import supot from "@/data/09support.js"

import NewsLetter from "./components/NewsLetter.vue"

import FooterView from "./components/FooterView.vue"
import FooterBottom from "@/components/FooterBottom.vue"


export default {
    components:{
    headerView,
    mainVisual,
    IconBanner,
    EduSlide,
    CountBanner,
    NoticeSlide,
    ResultView,
    VisualView,
    SupportView,
    NewsLetter,
    FooterView,
    FooterBottom
},
    data(){
       return{
        mslide:mslide,
        ibData:ibData,
        eduData:eduData,
        notice:notice,
        story:story,
        news:news,
        post:post,
        result:result,
        supot:supot,

       }
    }

}
</script>

<style>

</style>