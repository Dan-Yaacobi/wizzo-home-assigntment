<script setup>
  // Containers:
  import OtherArticles from '@/components/Containers/OtherArticles.vue'
  import TopArticles from '@/components/Containers/TopArticles.vue'
  import PodCasts from '@/components/Containers/PodCasts.vue'
  // import {Videos} from '@/components/Containers/Videos.vue'

  // Navigation Bars
  import TopNavBar from '@/components/Content/TopNavBar.vue'
  import BottomNavBar from '@/components/Content/BottomNavBar.vue'

  // Content:
    import Banner from '@/components/Content/Banner.vue'
    import MainArticle from './components/Content/MainArticle.vue'

  // Data:
    import articles from '@/assets/articles.json'
    import main_article from '@/assets/main_article.json'
    import podcasts from '@/assets/podcasts.json'


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
      <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#06c716"
    />

    <div class="hor_banner">
      <Banner
        src= 'src/assets/banner.png'
        width="855",
        height="150"
      />
    </div>

      <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#ff4fdf"
    />
    <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#06c716"
    />
    <div class="hor_banner">
      <Banner
        src= 'src/assets/banner.png'
        width="855",
        height="150"
      />
    </div>


      <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#ff4fdf"
    />
      <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#06c716"
    />
    <div class="hor_banner">
      <Banner
        src= 'src/assets/banner.png'
        width="855",
        height="150"
      />
    </div>

      <OtherArticles class="other_articles"
      :articles="articles",
      title="כותרת כלשהי על נדלן"
      tag="נדלן למגורים"
      color="#ff4fdf"
    />

    <PodCasts class="podcasts_page"
    :podcasts="podcasts"
    pod_title="פודקסטים"
    pod_tag="לעמוד המדור"
    color="#c4126d"/>

  </div>

    <BottomNavBar class="bottom_nav"/>
</template>

<style>
  .top_nav_bar{
    width: 100%;
  }
  .page {
    display: grid;
    grid-template-columns: 
      1fr
      minmax(0, 855px)
      1fr;
    background: #fbf8ff;
    padding: 50px;
  }
  .hor_banner{
    grid-column: 2;

  }
  .other_articles{
    grid-column: 2;
    margin-top: 50px;
    margin-bottom: 15px;
  }
  .top_articles{
    grid-column: 2 ;
  }
.podcasts_page{
  margin-top: 150px;
  margin-bottom: 150px;
  justify-content: center;
  grid-column: 2;
}
</style>