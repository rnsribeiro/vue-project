<script setup>
import { defineProps } from 'vue';

defineProps({
    nome: String,
    qtdCachorros: Number
})
</script>

<template>
    <div class="componente">
        <h1>Componente com Renderização Condicional</h1>
        <p>Nome: {{ nome }}</p>
        <p v-if="qtdCachorros === 0">Não tem cachorro</p>
        <p v-else-if="qtdCachorros === 1">Tem um cachorro</p>
        <p v-else>Tem muitos cachorros</p>
    </div>
</template>