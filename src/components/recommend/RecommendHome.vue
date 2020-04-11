<template>
    <div>
        <link rel="stylesheet" type="text/css"  href="/css/re_import.css">
        <link rel="stylesheet" type="text/css" href="/css/plugin/ion.rangeSlider.css">
        <link rel="stylesheet" type="text/css" href="/css/plugin/ion.rangeSlider.skinHTML5.css">
        <link rel="stylesheet"  type="text/css" href="/css/plugin/uniform.css">
        <link rel="stylesheet"  type="text/css" href="/css/plugin/jquery.scrollbar.css">
        <link rel="stylesheet" type="text/css"  href="/css/plugin/selectric.css">
        <link rel="stylesheet" type="text/css" href="/css/re_layout.css">
        <link rel="stylesheet" type="text/css" href=" /css/danawaCommon.css">
        <link rel="stylesheet" type="text/css" href=" /css/danawaCompare.css">
        <link rel="stylesheet" type="text/css" href="/css/danawaTheme.css">
        <link rel="stylesheet" type="text/css" href="/css/danawaHome.css">
        <link rel="stylesheet" type="text/css" href="/css/dnawaAuto.css">
        <Tab></Tab>
        <div class=" recommend">
        <router-view />
        </div>
    </div>
</template>
<script>

    import Tab from "@/components/recommend/RecommendTab.vue"

    export default{
        components:{Tab}
    }
</script>
<style scoped>
    .recommend{
        padding: 50px;
    }

</style>
