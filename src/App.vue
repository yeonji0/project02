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
       }
    }

}
</script>

<style>

</style>