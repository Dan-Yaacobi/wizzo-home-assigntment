<script setup>

</script>

<template>
    <nav class="navigation_bar">
        <div class="nav_image">
            <img src="/src/assets/main_logo.svg" alt="logo">
        </div>
        <div class="top_row">
            <div class="nav_social">

            </div>
            <div class="nav_buttons_top">
                <a href="">נדל״ן למגורים</a>
                <a href="">התחדשות עירונית</a>
                <a href="">נדל״ן מניב השקעות</a>
                <a href="">דעות וניתוחים</a>
                <a href="">חדשות הענף</a>
                <a href="">עיצוב ואדריכלות</a>
                <a href="">TV נדל״ן</a>
                <a href="">פודקאסטים</a>
            </div>


        </div>

        <div class="bottom_row">

            <div class="nav_search">
                <span class="search_icon"></span>
                <input type="text", placeholder="חיפוש">
            </div>

            <div class="nav_buttons_bottom">
                <a href="">מדד התחדשות עירונית</a>
                <a href="">מחשבונים</a>
                <a href="">נדל״ן בראש צעיר</a>
                <a href="">אודות מרכז הנדל״ן</a>
                <a href="">מכללת מרכז הנדל״ן</a>
                <a href="">צור קשר</a>
            </div>



        </div>
    </nav>
</template>

<style>
.nav_image{
    grid-column: 3;
    grid-row: 1 / span 2;

    display: flex;
    align-items: center;
    justify-content: flex-end;
    background-color: white;
    padding: 12px 12px; 
}
.nav_image img {
    height: 100%;
    max-height: 56px;
    width: auto;
}
.navigation_bar{
    display: grid;
    grid-template-columns: auto 1fr auto;
    grid-template-rows: auto auto;
    width: 100%;
}
.top_row {
    grid-column: 2;
    grid-row: 1;

    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 12px 12px;
    background: #5806c7;
    color: white;
    padding-right: 24px;
}

.nav_buttons_top {
    display: flex;
    gap: 16px;
    white-space: nowrap;
}

.bottom_row {
    grid-column: 2;
    grid-row: 2;

    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 12px 12px;
    background: white;
    color: black;
    padding-right: 24px;
    
}

.nav_buttons_bottom {
    display: flex;
    gap: 16px;
    white-space: nowrap;
}
.nav_image {
    justify-self: end;
}
.nav_search {
    grid-column: 1;
    grid-row: 2;

    display: flex;
    align-items: center;
    padding-left: 24px;
    width: 300px;
    height: 40px;
    border: 3px solid #f15723;
    border-radius: 500px;
    direction: rtl;
}
.nav_search input{
    border:none;
    outline:none;
    background: transparent;
    color:#f15723;
    padding-inline-start: 8px;
}
.nav_search ::placeholder{
    color:#f15723;
}
a {
    color: inherit;
    text-decoration: none;
    font-size: 14px;
}
</style>