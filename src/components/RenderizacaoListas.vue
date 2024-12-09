<script setup>
import { defineProps } from 'vue';

defineProps({
    nome: String,
    qtdCachorros: Array
})
</script>

<template>
    <div class="componente">
        <h1>Componente com Renderização de Lista</h1>
        <p>Nome: {{ nome }}</p>  
        <p v-show="qtdCachorros.length === 0">Não tem cachorro</p>
        <ul>
            <li v-for="cachorro in qtdCachorros">
                Nome: {{ cachorro.nome }} | Idade: {{ cachorro.idade }}
            </li>
        </ul>      
    </div>
</template>

<style scoped>
ul {
    margin: 0px;
    padding: 0px;
}

li {
    list-style-type: none;
    text-align: center;
    font-size: large;
}

</style>