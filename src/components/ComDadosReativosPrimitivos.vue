<script setup>
import { ref } from 'vue'

const nome = ref('Pedro')
const idade = ref(20)

function fazerAniversario() {
    //idade.value++
    idade.value += 1
}

function mudarNome() {
    nome.value = 'Ana'
}
</script>

<template>
    <div class="componente">
        <h1>Componente com Dados Reativos Primitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome">Mudar Nome</button>
    </div>
</template>

<style></style>