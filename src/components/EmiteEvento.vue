<template>
    <div class="componente">
        <h1>Componente que Emite Evento</h1>
        <p>{{ item }} (R${{ preco.toFixed(2) }})</p>
<!-- Abaixo na linha 6 abreviando [v-on :click], temos @click -->
        <button @click="adicionar">Adicionar ao Carrinho</button>
    </div>
</template>

<script setup>
import {defineProps, defineEmits} from "vue"

const props = defineProps({
    item:String,
    preco:Number
})

const emit = defineEmits(["ItemFoiAdicionado"])



function adicionar(){
    emit("ItemFoiAdicionado", props.preco)
}
</script>
