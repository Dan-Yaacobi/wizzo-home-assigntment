    <script setup>
        defineProps({
            main_article:{
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
        <div class="main_article_box">
            <div class="main_article_image">
                <img :src="main_article.src">
                <span class="tag" :style="{'--tag-color': color}">{{ main_article.tag }}</span>
            </div>

            <div class="text_area">
                <div class="top_data">
                    <span class="date">{{ main_article.date }}</span>
                    <span class="separator">|</span>
                    <span class="author">{{ main_article.author }}</span>

                </div>
                    <h3 class="main_title">{{ main_article.title }}</h3>
                    <h3 class="description">{{ main_article.description }}</h3>


            </div>

        </div>

    </template>

    <style>
        .main_article_box{
            display: flex;
            flex-direction: row;
            background:white;
            height: 100%;
            width: 100%;
            border-radius: 8px;
            overflow: hidden;
            color: black;
            direction: rtl;
            padding: 4px;
            border: 1px solid #ffffff;
        }

        .main_article_image{
            position: relative;
            height: 100%;
            width: 50%;
            
        }

        .main_article_image img{
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .text_area{
            width: 50%;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 16px;
        }
        .main_title{
            font-size: 20px;
            font-weight: bold;
        }
        .description{
            font-size: 14px;
            
        }
        .top_data{
            display: flex;
            justify-content: flex-start;
            align-items: center;
            gap: 6px;

            }
    </style>