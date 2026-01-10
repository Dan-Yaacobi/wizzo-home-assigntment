<script setup>
    defineProps({
        main_article:{
            type: Object,
            required: true
        },


        color:{
            type: String,
            default: '#000000'
        }

    })
</script>

<template>
    <div class="article_box">
        <div class="article_image">
            <img :src="article.src">
            <span class="tag" :style="{'--tag-color': color}">{{ main_article.tag }}</span>
        </div>

        <h3 class="title">{{ main_article.title }}</h3>

        <div class="bottom_data">
            <span class="date">{{ main_article.date }}</span>
            <span class="separator">|</span>
            <span class="author">{{ main_article.author }}</span>

        </div>
    </div>

</template>

<style>
    .article_box{
        display: flex;
        flex-direction: column;
        width:320px;
        height:300px;
        background:white;
        border-radius: 8px;
        overflow: hidden;
        color: black;
        direction: rtl;
        padding: 4px;

        border: 1px solid #ffffff;
    }

    .article_image{
        position: relative;
        height: 180px;
    }

    .article_image img{
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .tag {
        position: absolute;
        bottom: 0px;
        right: 0px;

        background: var(--tag-color);
        padding: 0px 20px;
        font-size: 12px;
        font-weight: bold;

    }

    .title{
        display: flex;
        justify-content: flex-start;
        font-size: 16px;
        line-height: 1.3;
    }
    .bottom_data{
        position: relative;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        gap: 6px;
        margin-top: auto;
        }
</style>