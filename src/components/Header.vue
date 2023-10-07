<template>
    <div class="header">
        <div class="header__container">
            <h1>Le partenaire de vos séjours sur mesure</h1>
            <p>
                Lorem ipsum dolor sit amet consectetur, adipisicinam omnis cupiditate ipsum esse tenetur dignissimos sunt.       Lorem ipsum dolor sit amet consectetur, adipisicinam omnis cupiditate ipsum esse tenetur dignissimos sunt.
                Lorem ipsum dolor sit amet consectetur, adipisicinam omnis cupiditate ipsum esse tenetur dignissimos sunt.
            </p>

            <div class="search__bar">
                <div class="search__bar__item localisation">
                    <img src="../assets/i-localisation.svg" alt="">
                    <input type="text" :value="destinationValue" @focus="clearValue('destinationValue')"
                        @blur="restoreValue('destinationValue', 'Destination, nom de l\'hôtel..')">
                </div>
                <div class="search__bar__item date">
                    <img src="../assets/i-date.svg" alt="">
                    <input type="text" :value="dateValue" @focus="clearValue('dateValue')"
                        @blur="restoreValue('dateValue', 'Arrivée - Départ')">
                </div>
                <div class="search__bar__item person">
                    <img src="../assets/i-person.svg" alt="">
                    <input type="text" :value="personValue" @focus="clearValue('personValue')"
                        @blur="restoreValue('personValue', '2 adultes - 1 chambre')">
                </div>
                <button type="submit">Rechercher</button>
            </div>
        </div>
    </div>

    <div class="card__info">
        <div class="card" v-for="(item, index) in Card" :key="index">
            <span class="title">{{ item.title }}</span>
            <span class="desc">{{ item.description }}</span>
        </div>
    </div>
</template>
  
<script setup>

import { ref } from 'vue';

const destinationValue = ref("Destination, nom de l'hôtel..");
const dateValue = ref("Arrivée - Départ");
const personValue = ref("2 adultes - 1 chambre");

function clearValue(refName) {
    const refValue = eval(refName);
    if (refValue) {
        refValue.value = "";
    }
}

function restoreValue(refName, defaultValue) {
    const refValue = eval(refName);
    if (refValue && refValue.value === "") {
        refValue.value = defaultValue;
    }
}

const Card = [
    { title: "Un large choix d'hôtel", description: "Lorem ipsum tetur, adipisicinam omnis cupiditate ipsum esse tenetur dignissimos sunt." },
    { title: "Tout en un", description: "Lorem ipsum tetur, adipisicinam omnis cupiditate ipsum esse tenetur dignissimos sunt." },
    { title: "Avis vérifiés", description: "Lorem ipsum tetur, adipisicinam omnis cupiditate ipsum esse tenetur dignissimos sunt." },
    { title: "Annulation gratuite", description: "Lorem ipsumtet ur, adipisicinam omnis cupiditate ipsum esse tenetur dignissimos sunt." }
];


</script>
  