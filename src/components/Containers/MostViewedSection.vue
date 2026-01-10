<script setup>
    import Article from '@/components/Content/Article.vue';
    import Banner from '@/components/Content/Banner.vue';
    defineProps({
        articles:{
            type: Array,
            default: []
        },
        title:{
            type: String,
            default: ''
        },
        color1:{
            type: String,
            default: '#000000'
        },
        color2:{
            type: String,
            default: '#000000'
        },
        color3:{
            type: String,
            default: '#000000'
        }
    })
</script>

<template>
<div class="most_viewed_container">
    <Article :article="articles[0]" :color ="color1"/>
    <Article :article="articles[1]" :color ="color2"/>
    <Banner class="vert_banner" 
    src="/src/assets/vert_banner.png"
    width="200"
    height="200"
    />
    <Article :article="articles[2]" :color ="color2"/>

</div>

</template>

<style>
.most_viewed_container{
    display:grid;
    grid-template-columns: repeat(1 ,1fr);
    gap: 5px;
}

</style>