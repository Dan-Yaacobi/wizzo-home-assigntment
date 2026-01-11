<script setup>
    //component
    import PodCast from '../Content/PodCast.vue';


    defineProps({
        podcasts:{
            type: Array,
            default: []
        },
        pod_title:{
            type: String,
            default: ''
        },
        pod_tag:{
            type: String,
            default: ''
        },
        color:{
            type: String,
            default: '#000000'
        }
    })
</script>

<template>
    <div class="container">
        <div class="top_title">
            <div class="articles_tag" :style="{'--tag-color': color}">{{ pod_tag }}</div>
            <span class="line" :style="{'--tag-color': color}"></span>
            <h1 class="articles_title">{{ pod_title }}</h1>
            <span class="mini_logo" :style="{'--tag-color': color}">
                <img src="/src/assets/mini_logo.svg" alt="">
            </span>
        </div>
        <div class="podcasts">
            <PodCast v-for="podcast in podcasts.slice(0,4)" :key="podcast.id" :podcast="podcast" :color ="color"/>
        </div>

    </div>


</template>

<style>


.podcasts{
    margin-top: 20px;
    display: grid;
    grid-template-columns: repeat(2,1fr);
    gap: 10px;
    width: 870px;
}
</style>