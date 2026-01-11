<script setup>

</script>

<template>
    <div class="bottom_nav_container">
        <div class="top_cropped">
            <span class="bottom_nav_logo">
                <img src="/src/assets/main_logo.svg" alt="">
            </span>
            <div class="social icons">

            </div>
        </div>


        <div class="bottom_nav_coloumns">
            <div class="column">
                <div class="column_title">כותרת 1</div>
                <a href="">נדל״ן למגורים</a>
                <a href="">התחדשות עירונית</a>
                <a href="">נדל״ן מניב השקעות</a>
                <a href="">דעות וניתוחים</a>
                <a href="">חדשות הענף</a>
                <a href="">עיצוב ואדריכלות</a>
                <a href="">TV נדל״ן</a>
                <a href="">RSS</a>
                <a href="">צור קשר</a>
                <a href="" style="color: red;">v קרא עוד</a>
            </div>
                <div class="column">
                    <div class="column_title">כותרת 2</div>
                    <a href="">נדל״ן למגורים</a>
                    <a href="">התחדשות עירונית</a>
                    <a href="">נדל״ן מניב השקעות</a>
                    <a href="">דעות וניתוחים</a>
                    <a href="">חדשות הענף</a>
                    <a href="">עיצוב ואדריכלות</a>
                    <a href="">TV נדל״ן</a>
                    <a href="">RSS</a>
                    <a href="">צור קשר</a>
                    <a href="" style="color: red;">v קרא עוד</a>
            </div>
                <div class="column">
                    <div class="column_title">כותרת 3</div>
                    <a href="">נדל״ן למגורים</a>
                    <a href="">התחדשות עירונית</a>
                    <a href="">נדל״ן מניב השקעות</a>
                    <a href="">דעות וניתוחים</a>
                    <a href="">חדשות הענף</a>
                    <a href="">עיצוב ואדריכלות</a>
                    <a href="">TV נדל״ן</a>
                    <a href="">RSS</a>
                    <a href="">צור קשר</a>
                    <a href="" style="color: red;">v קרא עוד</a>
            </div>
                <div class="column">
                    <div class="column_title">כותרת 4</div>
                    <a href="">נדל״ן למגורים</a>
                    <a href="">התחדשות עירונית</a>
                    <a href="">נדל״ן מניב השקעות</a>
                    <a href="">דעות וניתוחים</a>
                    <a href="">חדשות הענף</a>
                    <a href="">עיצוב ואדריכלות</a>
                    <a href="">TV נדל״ן</a>
                    <a href="">RSS</a>
                    <a href="">צור קשר</a>
                    <a href="" style="color: red;">v קרא עוד</a>
            </div>
        </div>

        <div class="bottom_nav_info"> 
            <div>כל הזכויות שמורות למישהו</div>
            <div>איזו כותרת מסויימת אחרת</div>
            <div>איזו כותרת מסויימת</div>



        </div>


    </div>
</template>

<style>
.bottom_nav_container {
    display: flex;
    flex-direction: column;
    align-items: center;
    background: linear-gradient(180deg, #5b14c9, #4b0fb3);
    color: white;
}
.top_cropped{
    padding: 10px;
    background: #fbf8ff;

}
.bottom_nav_logo img{
    width: 150px;

}


.bottom_nav_coloumns {
    padding: 40px 10px;
    width: 870px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 40px;
}
.column_title{
    font-weight: bold;
    font-size: 24px;
}
.column {
    display: flex;
    flex-direction: column;
    gap: 10px;
}
.bottom_nav_info{
    background-color: black;
    display: flex;
    justify-content: center;
    margin-top: 30px;
    padding: 20px 20px;
    gap: 100px;
    width: 100%;
}
</style>