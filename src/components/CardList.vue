<template>
    <div class="cardlist">
        <div class="header__cardlist">
            <span>Showing <strong>127</strong>Jobs</span>
            <div class="sort">
                <span>Sort by :</span>
                <span>Newest </span>
                <img src="../assets/i-arrow.svg" alt="">
            </div>
        </div>
        <div class="cardlist__container">
            <Card />
            <Card />
            <Card />
            <Card />
        </div>

        <div class="premium">
            <div class="premium__container">
                <div class="premium__content">
                    <h3>Get premium to receive customized offers, automate your job search, receive notifications and much
                        more.
                    </h3>
                    <p>Our plans are affordable and customizable, check them out !</p>
                </div>
                <button>Go Premium</button>
            </div>
        </div>

        <div class="pagination">
       
                <img src="../assets/i-arrow.svg" alt="">
                <button class="active">1</button>
                <button>2</button>
                <button>3</button>
                <span>...</span>
                <button>12</button>
                <img class="arrow__pagination" src="../assets/i-arrow.svg" alt="">
    
        </div>
    </div>
</template>

<script setup>

import Card from '../components/Card.vue';

</script>
