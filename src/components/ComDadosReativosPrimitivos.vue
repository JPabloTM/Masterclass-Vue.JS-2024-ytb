<template>
    <div class="componente">
        <h1>Componente com Dados Reativos Primitivos</h1>
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazerAniversário()">Fazer Aniversário</button>
        <button v-on:click="mudarNome()">Mudar Nome</button>
    </div>
</template>


<script setup>
import {ref} from "vue"

    const nome = ref("Ana")
    const idade = ref(27)

    function fazerAniversário(){
        idade.value += 1
    }
    function mudarNome(){
        nome.value = "Jonathan Pablo"
    }
</script>


<style>

</style>