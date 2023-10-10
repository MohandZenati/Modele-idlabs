<script setup>
import Navbar from './components/Navbar.vue';
import Searchbar from './components/Searchbar.vue';
import FilterList from './components/FilterList.vue';
import CardList from './components/CardList.vue';
import Footerbar from './components/Footerbar.vue';

</script>

<template>
    <main>
        <Navbar />
        <Searchbar />
        <div class="content">
            <FilterList />
            <CardList />
        </div>
        <Footerbar />
    </main>
</template>
