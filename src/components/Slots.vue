<script setup></script>

<!-- MODELO COM SLOTS NOMEADOS -->
<template>
    <div class="componente">
        <h1>Componente com Slots</h1>
        <button><slot name="icone" /> <slot name="texto"/></button>
    </div>
</template>

<!-- MODELO COM SLOT FIXO
<template>
    <div class="componente">
        <h1>Componente com Slots</h1>
        <button><slot></slot></button>
    </div>
</template> -->

