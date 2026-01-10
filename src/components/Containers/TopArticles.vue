<script setup>
// components
import MostViewedSection from './MostViewedSection.vue';
import MainArticle from '../Content/MainArticle.vue';
import Article from '../Content/Article.vue';
import Banner from '../Content/Banner.vue';

//data
import articles from '@/assets/articles.json'
import main_article from '@/assets/main_article.json'

</script>

<template>
    <div class="top_articles_container">

        <div class="left_section">
            <MostViewedSection
            :articles="articles"
            title="הכתבות הנצפות ביותר"
            color1="#ff63b4"
            color2="#63ffff"
            color3="#febfff"
            />

        </div>
        <div class="divider"></div>
        <div class="right_section">
            <Banner
            src= 'src/assets/banner.png'
            width="605"
            height="100"/>

            <MainArticle class="main_article"
                :main_article="main_article"
                color="#f5c400"
                />

            <div class="top_articles_regular">
                <Article v-for="article in articles" :key="article.id" :article="article" :color ="article.color"/>

            </div>

            <Banner
            src= 'src/assets/banner.png'
            width="605"
            height="100"/>
        </div>


    </div>


</template>

<style>
.top_articles_container{
    display: grid;
    grid-template-columns: 1fr 1px 3fr;
    gap: 24px;
    width: 100%;
}
.top_articles_regular{
    display: grid;
    grid-template-columns: repeat(3, 0fr);
    grid-template-rows: auto auto;
    gap: 5px;

}
.top_articles{
    display: grid;
    gap: 24px;
    width: 70%;
}

.right_section{
    display: flex;
    flex-direction: column;
    height: 100%;
    width: 100%;
}

.divider{
    background: #000000;
}
.left_section{
    display: flex;
    flex-direction: column;
}

</style>