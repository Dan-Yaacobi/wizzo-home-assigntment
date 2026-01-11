<script setup>
    import Article from '@/components/Content/Article.vue';

    defineProps({
        articles:{
            type: Array,
            default: []
        },
        title:{
            type: String,
            default: ''
        },
        tag:{
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
            <div class="articles_tag" :style="{'--tag-color': color}">{{ tag }}</div>
            <span class="line" :style="{'--tag-color': color}"></span>
            <h1 class="articles_title">{{ title }}</h1>
            <span class="mini_logo" :style="{'--tag-color': color}">
                <img src="/src/assets/mini_logo.svg" alt="">
            </span>
        </div>

        <div class="articles_box">
            <Article v-for="article in articles.slice(0,4)" :key="article.id" :article="article" :color ="color"/>
        </div>
    </div>
</template>

<style>

    .articles_box {
        display: flex;
        justify-content: space-between;
        padding-top: 12px;

    }
    .mini_logo{
        filter: drop-shadow(-2px 3px 0 var(--tag-color));   
        margin-left: 12px;
    }
    .mini_logo img{
        height: 40px;
        width: auto;
        display: block;
    }
    .top_title{
        display: flex; 
        font-size: 10px;
        font-weight: bold;
        
        height: auto;
        align-items: baseline;
        color: black;
    }

    .articles_tag {
        background: var(--tag-color);
        font-size: 12px;
        padding: 0px 20px;
        font-weight: bold;

        clip-path: polygon(
        10px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 10px)
    }
    .line {
        flex-grow: 1;
        height: 2px;
        background: var(--tag-color);
        margin: 0px 70px;
        margin-left: 5px;
    }   
</style>