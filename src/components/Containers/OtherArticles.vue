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

        </div>

        <div class="articles_box">
            <Article v-for="article in articles.slice(0,4)" :key="article.id" :article="article" :color ="color"/>
        </div>
    </div>
</template>

<style>
    /* .container{
        width: 80%;
    } */
    .articles_box {
        display: flex;
        justify-content: space-between;
        /* padding: 10px;*/
        padding-top: 20px;

    }

    .top_title{
        display: flex; 
        font-size: 10px;
        font-weight: bold;
        
        width: 100%;
        height: auto;
        align-items: baseline;
        color: black;
    }

    .articles_tag {
        background: var(--tag-color);
        font-size: 12px;
        padding: 0px 20px;
        font-weight: bold;
    }
    .line {
        flex-grow: 1;
        height: 2px;
        background: var(--tag-color);
        margin: 0px 80px;
        margin-left: 5px;
    }   
</style>