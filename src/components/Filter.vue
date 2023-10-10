<template>
  <div class="filter__content" v-for="(item, index) in nameFilter" :key="item.name">
    <div class="title">
      <h1>{{ item.name }}</h1>
      <img src="../assets/i-arrow.svg" alt="">
    </div>

    <div class="searchcity" v-if="index === 0">
      <img src="../assets/i-search.svg" alt="">
      <input type="text" value="City name...">
    </div>

    <div class="filter__option"> 
      <div class="filter" v-for="(dataItem, dataIndex) in item.data" :key="dataIndex">
        <div class="filter__item" >
          <input type="checkbox" :value="dataItem.title">
          <label>{{ dataItem.title }}</label>
        </div>
        <span>{{ dataItem.numbers }}</span>
      </div>

    </div>
  </div>
</template>

  
  <script setup>

  const city = [
    { title: "Paris", numbers: "87" },
    { title: "Marseille", numbers: "65" },
    { title: "Lyon", numbers: "23" },
    { title: "Lille", numbers: "34" },
    { title: "Bordeaux", numbers: "65" },
  ];
  
  const Categorie = [
    { title: "Front-end", numbers: "57" },
    { title: "back-end", numbers: "15" },
    { title: "Mobile", numbers: "32" },
    { title: "UX/UI Design", numbers: "28" },
    { title: "Project Management", numbers: "10" },
  ];
  
  const jobType = [
    { title: "Full time", numbers: "57" },
    { title: "Part time", numbers: "15" },
    { title: "Full remote", numbers: "32" },
    { title: "Intership", numbers: "28" },
    { title: "Apprentice", numbers: "10" },
  ];

  const Equipment = [
    { title: "Babyfoot", numbers: "5" },
    { title: "Microwave", numbers: "9" },
    { title: "Standing", numbers: "2" },
    { title: "Sofa", numbers: "14" },
    { title: "Kitchen", numbers: "19" },
  ];
  
  
  const nameFilter = [
    { name: "City", data: city },
    { name: "Categorie", data: Categorie },
    { name: "Job Type", data: jobType },
    { name: "Equipment", data: Equipment },
  ];
  
  

  </script>
  