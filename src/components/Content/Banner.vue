<script setup>
    defineProps({
        src: {
            type: String,
            required: true
        },
        alt:{
            type: String,
            default: ''
        },
        height:{
            type :Number,
            required: true
        },
        width:{
            type :Number,
            required: true
        }
    })
</script>

<template>
    <div class="banner_image" :style="{width: width +'px', height: height +'px'}">
        <img :src="src" :alt="alt">
    </div>

</template>

<style>

    .banner_image img{
        width: 100%;
        height: 100%;
    }
</style>