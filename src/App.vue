<template>
<header-view></header-view>
<main-visual v-bind:mslide="mslide"></main-visual>
<icon-banner :ibData="ibData"></icon-banner>
</template>

<script>
import "@/assets/style.css"

import headerView from "@/components/headerView.vue"

import mainVisual from "@/components/mainVisual.vue"
import mslide from "./data/01mainSlide.js"

import IconBanner from "@/components/IconBanner.vue"
import ibData from "./data/02iconBanner.js"

export default {
    components:{
        headerView,
        mainVisual,
        IconBanner,
    },
    data(){
       return{
        mslide:mslide,
        ibData:ibData,

       }
    }

}
</script>

<style>

</style>