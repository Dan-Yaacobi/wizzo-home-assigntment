<script setup>
  // // Containers:
  import MostViewedSection from '@/components/Containers/MostViewedSection.vue'
  import OtherArticles from '@/components/Containers/OtherArticles.vue'
  import TopArticles from '@/components/Containers/TopArticles.vue'
  // import {PodCasts} from '@/components/Containers/PodCasts.vue'
  // import {Videos} from '@/components/Containers/Videos.vue'

  // // Navigation Bars
  import TopNavBar from '@/components/Content/TopNavBar.vue'
  // import {BottomNavBar} from '@/components/Content/BottomNavBar.vue'
  // Banner:
    import Banner from '@/components/Content/Banner.vue'

  // Data:
    import articles from '@/assets/articles.json'
    import main_article from '@/assets/main_article.json'

    import MainArticle from './components/Content/MainArticle.vue'

</script>

<template>

  
  <div class="top_nav_bar">
    <TopNavBar/>
  </div>

  <div class="page">
      
    <div class="top_articles">
      <TopArticles/>
    </div>

    <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#f5c400"
    />
    <div class="hor_banner">
      <Banner
        src= 'src/assets/banner.png'
        width="500",
        height="150"
      />
    </div>
    <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#06c716"
    />
  </div>

</template>

<style>
  .top_nav_bar{
    width: 100%;
  }
  .page {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    background: #fbf8ff;
  }
  .hor_banner{
    grid-column: 2;

  }
  .other_articles{
    grid-column: 2 / span 2;
  }
  .top_articles{
    grid-column: 2 /span 3;
  }
</style>