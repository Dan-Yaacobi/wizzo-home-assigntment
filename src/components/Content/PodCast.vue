<script setup>
    defineProps({
        podcast:{
            type: Object,
            required: true
        },
        color:{
            type: String,
            default: '#ffffff'
        }
    })
</script>

<template>
    <div class="podcast_box">
        <div class="podcast_image">
            <img :src="podcast.src">
            <span class="tag" :style="{'--tag-color': color}">{{ podcast.tag }}</span>
        </div>

        <div class="podcast_icons">
            
        </div>

        <div class="text_area">
                <h4 class="podcaster_name">{{ podcast.name }}</h4>
                <h5 class="podcaster_title">{{ podcast.title }}</h5>
                <h5 class="podcast_description">{{ podcast.description }}</h5>

        <div class="bottom_data">

                <span class="date">{{ podcast.date }}</span>
                <span class="separator">|</span>
                <span class="author">{{ podcast.author }}</span>
                <span class="separator">|</span>
                <span >פודקסטים</span>

            </div>

        </div>

    </div>

</template>

<style>
.podcast_image {
    position: relative;
    display: flex;
}
.podcast_image img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    border-radius: 6px;
    display: block;
}
.podcast_box {
    display: flex;
    direction: rtl;
    height: 150px;
    width: 430px;
    background: white;
    padding: 8px;
    border-radius: 8px;
}
.text_area {
    flex: 1;
    display: flex;
    flex-direction: column;
    /* justify-content: space-evenly; */
    overflow: hidden;
    color: black;
}
.podcaster_name{
    font-size: 20px;
    font-weight: bold;
}
.podcaster_title{
    font-weight: bold;
}
</style>