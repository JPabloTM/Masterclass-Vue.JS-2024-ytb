<template>
    <div class="componente">
        <h1>Componente que Escuta Evento</h1>
        <p>Total: R${{ total }}</p>
    
        <div class="lista">
            <EmiteEvento item="Item 1" :preco="1.99" @ItemFoiAdicionado="atualizarTotal"/>
            <EmiteEvento item="Item 2" :preco="5.00" @ItemFoiAdicionado="atualizarTotal"/>
            <EmiteEvento item="Item 3" :preco="10.99" @ItemFoiAdicionado="atualizarTotal"/>
        </div>
</div>
</template>

<script setup>
import EmiteEvento from "./EmiteEvento.vue"
import {ref} from "vue"
const total = ref(0)

function atualizarTotal(p){
    const valor = total.value + p
    // Obs. A Linha 22 retorna uma String, ao adicionar_
    // um [+] abaixo, convertemos uma String para um número
    total.value = +valor.toFixed(2)
}
</script>

<style scoped>
.lista {
    display: flex;
    justify-content: space-between;
}
</style>