<template>
    <!--     
    <div class="card__info">
        <div class="card" v-for="(item, index) in Card" :key="index">
            <span class="title">{{ item.title }}</span>
            <span class="desc">{{ item.description }}</span>
        </div>
    </div> -->

    <div class="hotel__card" v-for="(item,index) in HotelCard" :key="index">
        <img src="../assets/bg-hotel.jpg" alt="">
        <div class="hotel__card__info">
            <span>{{ item.title }}</span>
            <div class="card__column">
                <span><strong>{{ item.city }}</strong></span>
                <span>{{ item.notice }}/5 (98 Avis)</span>
            </div>
            <span>à partir de <strong>{{ item.price }}</strong></span>
        </div>
    </div>
</template>
  
<script setup>
const HotelCard = [
    { title: "Private Cost Hotel", city: "Carcasonne", notice:"4,9", price:"432€" },
    { title: "Private Cost Hotel", city: "Carcasonne", notice:"4,9", price:"432€" },
    { title: "Private Cost Hotel", city: "Carcasonne", notice:"4,9", price:"432€" },
    { title: "Private Cost Hotel", city: "Carcasonne", notice:"4,9", price:"432€" }

];


</script>
  