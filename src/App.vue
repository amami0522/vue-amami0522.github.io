<template>
    <div id="app">
        <title-background/>
        <icons/>
        <introduction/>
        <skill/>
        <draw/>
        <product/>
        <participation/>
        <other/>
        <copyright-footer/>
    </div>
</template>

<script>
import titleBackground from "@/components/titleBackground";
import icons from "@/components/icons";
import introduction from "@/components/introduction";
import skill from "@/components/skill";
import draw from './components/draw.vue';
import product from "@/components/product";
import participation from "@/components/participation";
import other from "@/components/other";
import copyrightFooter from "@/components/copyrightFooter";

export default {
    name: 'App',
    components: {
        titleBackground,
        icons,
        introduction,
        skill,
        draw,
        product,
        participation,
        other,
        copyrightFooter
    }
}
</script>

<style>
#app {
    font-family: "Yu Gothic UI", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin: 0;
    background: #F4F9F9;
}
</style>
