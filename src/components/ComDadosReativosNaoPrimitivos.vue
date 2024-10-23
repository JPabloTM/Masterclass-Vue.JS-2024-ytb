<template>
    <div class="componente">
        <h1>Componente com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>

        <!-- Uma outra forma de fazer o (v-on:click) usando o "@" -->
        <button @click="fazerAniversario()">Fazer Aniversário</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<!-- utilizando a (options API <script setup>)

<script setup>
import {reactive} from "vue"

    const pessoa = reactive({nome: "Ana", idade: 27})

    function fazerAniversário(){
        pessoa.idade += 1
    }
    function mudarNome(){
        pessoa.nome = "Jonathan Pablo"
    }
</script> -->


<!-- utilizando a (options API) na tag script -->

<script>
export default{
    data:function (){
        return {
            pessoa:{
                nome: "Ana",
                idade:27
            }
        }
    },
    methods:{
        fazerAniversario:function(){
            this.pessoa.idade +=1
        },
        mudarNome:function(){
            this.pessoa.nome = "Jonathan Pablo"
        }
    }
}
</script>
