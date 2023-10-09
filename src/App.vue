<script setup>
import Navbar from './components/Navbar.vue';
import Searchbar from './components/Searchbar.vue';
import FilterList from './components/filterlist.vue';
import CardList from './components/CardList.vue';
import Footerbar from './components/Footerbar.vue';

</script>

<template>
    <Navbar />
    <Searchbar />
    <div class="content">
        <filterList />
        <CardList />
    </div>
    <Footerbar />

    

</template>
