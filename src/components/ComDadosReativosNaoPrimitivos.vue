<!-- <script setup>
import { reactive } from 'vue';

const pessoa = reactive({
    nome: 'Pedro',
    idade: 20
})

function fazerAniversario() {
    //idade.value++
    pessoa.idade += 1
}

function mudarNome() {
    pessoa.nome = 'Ana'
}
</script> -->

<!-- SCRIPT COM OPTIONS API -->
<script>
export default {
    data: function() {
        return {
            pessoa: {
                nome: 'Pedro',
                idade: 20
            }
        }
    },
    methods: {
        fazerAniversario() {
            this.pessoa.idade++
        },
        mudarNome() {
            this.pessoa.nome = 'Ana'
        }
    }
}
</script>

<template>
    <div class="componente">
        <h1>Componente com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
        <button @click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome">Mudar Nome</button>
    </div>
</template>

<style></style>