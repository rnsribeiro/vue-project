<!-- PROPRIEDADES ASSISTIDAS USANDO WATCH -->
<!-- <script setup>
import { ref, watch } from 'vue'

const anoNascimento = ref(1900)
const anoAtual = ref(2024)
const idade = ref(0)

watch(anoAtual, (ano) => {
    idade.value =  ano - anoNascimento.value
})

watch(anoNascimento, (ano) => {
    idade.value = anoAtual.value - ano
})
</script> -->

<!-- PROPRIEDADES ASSISTIDAS USANDO WATCHEFFECT -->
<script setup>
import { ref } from 'vue'
import { watchEffect } from 'vue'

const anoNascimento = ref(1900)
const anoAtual = ref(2024)
const idade = ref(0)

watchEffect(() => {
    idade.value = anoAtual.value - anoNascimento.value
})
</script>

<template>
    <div class="componente">
        <h1>Componente com Propriedades Assistidas</h1>
        <p>{{ idade }}</p>
        <label>Ano Nascimento:</label>
        <input type="number" v-model="anoNascimento" min="2000">
        <label>Ano Atual:</label>
        <input type="number" v-model="anoAtual" min="2000">
    </div>
</template>

<style scoped>
label {
    margin: 10px;
}
</style>