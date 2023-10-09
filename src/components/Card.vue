<template>
    <div class="card" v-for="item in Card" :key="item.data">
        <div  class="card__top">
            <img :src="item.icon" alt="Logo" />
            <img src="../assets/i-menu.svg" alt="">
        </div>
        <div class="card__content">
            <h2>{{ item.title}}</h2>
            <p>{{ item.desc }}</p>
            <div class="buttons">
                <button>Apply</button>
                <button>View</button>
            </div>
        </div>
    </div>
</template>

<script setup>

import Logo1 from "../assets/i-logo-2.svg"
import Logo2 from "../assets/i-logo-3.svg"
import Logo3 from "../assets/i-logo-4.svg"

const Card = [
    { icon: Logo1, title: "Junior Front Developer", desc: "IDLABS is a development studio that strives its customers with powerful and friendly user experiences" },
    { icon: Logo2, title: "Web Developer", desc: "At Google, we are preparing our interfaces and products for the next billion users that are going to revolution..." },
    { icon: Logo3, title: "Mobile & Front-End Developer", desc:" Trello is the best task management tool-join our team to discover our methods and improve our product" },
];







</script>
