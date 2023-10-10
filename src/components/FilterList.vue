<template>
    <div class="filterbar">
      <div class="filterbar__container">
        <Filter />
      </div>
    </div>
  
    <div class="btn__filterbar__container">
      <button @click="toggleFilter" class="btn__filter">
        <img src="../assets/i-filter.svg" alt="">
        <span>Filters</span>
      </button>
  
      <div class="btn__filterbar__content">
        <div  @click="toggleFilter" class="btn__filterbar__header">
          <img src="../assets/i-arrow.svg" alt="">
          <span>Retour</span>
        </div>   
        <div class="filterbar__container">
          <Filter />
          <button>Apply Filters</button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import Filter from '../components/Filter.vue';
  
  function toggleFilter() {
    let popup = document.querySelector(".btn__filterbar__content");
    popup.classList.toggle("open");
  }
  </script>
  