<template>
    <div class="filterbar">
        <div class="filterbar__container">
            <Filter />         
        </div>
    </div>

    <button class="btn__filter">
        <img src="../assets/i-filter.svg" alt="">
        <span>Filters</span>
    </button>
</template>

<script setup>
import Filter from '../components/Filter.vue';

</script>
