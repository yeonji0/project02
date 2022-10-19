<template>
<div class="slideWrap">
    <div class="container">
        <h1>JA 기관소식</h1>
        <div class="row">
            <div class="col">공지사항</div>
            <div class="col">스토리</div>
            <div class="col">언론보도</div>
        </div>
        <notice-slide-tap></notice-slide-tap>
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
        "news"
    ],

}
</script>

<style lang="scss">

</style>