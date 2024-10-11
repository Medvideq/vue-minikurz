<script setup>
    import {ref} from "vue";
    
    let casovac = ref(10);


    const interval = setInterval(() => {
        casovac.value--;
        if (casovac.value <= 0) {
            casovac.value = "Hotovo!";
            clearInterval(interval);
        }
    }, 1000);

</script>

<template>
    <p>Odpocet: {{ casovac }}</p>
</template>

<style scoped>
    p {
        color: lightcyan;
    }
</style>