<script setup>
    defineProps({
        article:{
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
            <span class="tag" :style="{'--tag-color': color}">{{ article.tag }}</span>
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
        width:200px;
        height:200px;
        
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
        height: 110px;
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

        clip-path: polygon(
        10px 0,
        100% 0,
        100% 100%,
        0 100%,
        0 10px
    );

    }

    .title{
        display: flex;
        justify-content: flex-start;
        font-size: 12px;
        line-height: 1.3;
        font-weight: bold;
    }
    .bottom_data{
        position: relative;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        gap: 3px;
        margin-top: auto;
        font-size: 12px;
        color: #9b9b9bd7;
        }
</style>