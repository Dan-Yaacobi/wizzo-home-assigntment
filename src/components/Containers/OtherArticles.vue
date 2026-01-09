<script setup>
    import Article from '@/components/Content/Article.vue';
    import { ref } from 'vue';

    const title = ref('נדלן למגורים')
    const tag = ref('< לעמוד מדור')
</script>

<template>
    <div class="container">
        <div class="top_title">
            <div class="articles_tag">{{ tag }}</div>
            <span class="line"></span>
            <h1 class="articles_title">{{ title }}</h1>

        </div>

        <div class="articles_box">
            <Article/>
            <Article/>
            <Article/>
            <Article/>
        </div>
    </div>
</template>
<style>
    .container{
        background-color: white;
    }
    .articles_box {
        display: flex;
        gap: 12px;
        padding: 10px;
        padding-top: 20px;
    }

    .top_title{
        display: flex;  
        justify-content: space-between;
        width: 100%;
        height: auto;
        align-items: baseline;
        color: black;
    }

    .articles_tag {
        background: #f5c400;
        font-size: 12px;
        padding: 0px 20px;
        font-weight: bold;
    }
    .line {
        flex-grow: 1;
        height: 2px;
        background: #f5c400;
        margin: 0px 120px;
        margin-left: 5px;
    }   
</style>