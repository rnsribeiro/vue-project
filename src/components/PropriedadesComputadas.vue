<script setup>
import { ref, computed } from 'vue'

const anoNascimento = ref(1900)
const anoAtual = ref(2000)
const idade = computed(() => {
    return anoAtual.value - anoNascimento.value
})
</script>

<template>
    <div class="componente">
        <h1>Componente com Propriedades Computadas</h1>
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