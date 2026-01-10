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
    <Article :article="articles[0]" :color ="color1"/>
    <Article :article="articles[1]" :color ="color2"/>
    <Banner 
    src="/src/assets/vert_banner.png"
    />
    <Article :article="articles[2]" :color ="color2"/>
</template>