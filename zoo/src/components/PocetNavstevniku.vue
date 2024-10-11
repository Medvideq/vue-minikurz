<script setup>
//funkce ref je exkluzivni pro vue, proto ji musime naimportovat
import {ref} from "vue";

//zadame vychozi hodnotu
const pocet = ref(100);

//ukazeme si reaktivitu na intervalu
setInterval(() => {
    //kdykoliv budeme chtit cist nebo menit hodnotu reaktivni promenne, tak musime jit pres vlastnost value
    pocet.value = Math.floor(Math.random() * 10000);
}, 2000);

</script>

<template>
    <!-- double mustache rika ze zde se ma vypast nejaka reaktivni hodnota -->
    <!-- double mustache nemuzete pouzit v atributu elementu, musi byt vzdy mezi tagama -->
    <p>Pocet navstevniku: {{ pocet }}</p>
</template>

<style scoped>
    p {
        color: lightcyan;
    }
</style>