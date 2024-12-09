<script setup>
import { ref } from 'vue'
const valor = ref("Vue é muito legal")
</script>

<template>
    <div class="componente">
        <h1>Componente com Data Binding</h1>
        <p>{{ valor }}</p>
        <!-- ONEWAY DATA BINDING -->
        <!-- <input type="text" v-bind:value="valor"></input> -->

        <!-- TWOWAY DATA BINDING -->
        <!-- <input type="text" v-bind:value="valor" v-on:input="valor = $event.target.value"></input> -->

        <!-- TWOWAY DATA BINDING SHORT SYNTAX -->
        <!-- <input type="text" :value="valor" @input="valor = $event.target.value"></input> -->

        <!-- TWOWAY DATA BINDING SHORT SYNTAX COM VUE 3 -->
        <input type="text" v-model="valor"></input>
    </div>
</template>