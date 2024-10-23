<template>
    <div class="componente">
        <h1>Componente com Data Binding</h1>
        <p>{{ valor }}</p>
        <!--_____________one way Data Binding________________-->
        <!-- <input type="text" v-bind:value="valor"><input> -->

    
        <!--___________two way Data Binding sem atalhos_________-->
        <!-- <input type="text" v-bind:value="valor"
        v-on:input="(e)=>valor = e.target.value"><input>        -->


        <!--_________two way Data Binding com atalhos_________-->
        <!-- <input type="text" :value="valor"
        @input="(e)=>valor = e.target.value"></input>         -->

        <!-- __________________v-model_______________________ -->
        <input type="text" v-model="valor"></input>

    </div>
</template>

<script setup>
import {ref} from "vue"
const valor = ref("Vue é muito Legal!")
</script>