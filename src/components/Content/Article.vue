<script setup>
   import { ref } from 'vue';

    const article = ref({
        tag: "נדלן למגורים",
        title: "עוד פעם הדירות יקרות מידי, מה יהיה?",
        date: "05-09",
        author: "דן נדלן",
        image: "@assets/realestate.jpeg"
    })

</script>

<template>
    <div class="article_box">
        <div class="article_image">
            <img src="/src/assets/realestate.jpg">
            <span class="tag">{{ article.tag }}</span>
        </div>

        <h3 class="title">{{ article.title }}</h3>

        <div class="bottom_data">
            <span class="date">{{ article.date }}</span>
            <span class="separator">|</span>
            <span class="author">{{ article.author }}</span>

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

        background: #f5c400;
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