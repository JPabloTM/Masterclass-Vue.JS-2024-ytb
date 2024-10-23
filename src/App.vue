<script setup>
import PrimeiroComponente from "./components/PrimeiroComponente.vue"
import ComDados from "./components/ComDados.vue"
import ComDadosReativosPrimitivos from "./components/ComDadosReativosPrimitivos.vue"
import ComDadosReativosNaoPrimitivos from "./components/ComDadosReativosNaoPrimitivos.vue"
import DataBinding from "./components/DataBinding.vue"
import ComProps from "./components/ComProps.vue"
import EscutaEvento from "./components/EscutaEvento.vue"

// // Atribuindo valores const no script (props) 
// obs. precisa utilizar v-binding para isso data, | *Comentario[01]
const borracha = "Borracha"
const precoBorracha = 2.50
</script>

<template>
  <header>Vue</header>
  <EscutaEvento/>
  
  <!-- Comentario[01] | Obs. Posso atribuir valores como dados hardcoded da forma abaixo
  ou definindo constantes no script da forma que está rodando e não está comentada!

  <ComProps item="Apontador" v-bind:preco="1.99"/>
  <ComProps item="Caderno" v-bind:preco="10.25"/>
  <ComProps item="Borracha" v-bind:preco="2.50"/> -->


  <!-- Posso omitir o v-bind e usar dois pontos, dessa forma:                        v                 v
  [<ComProps item = "borracha" v-bind:preco="precoBorracha"/> ]   para   [<ComProps :item = "borracha" :preco="precoBorracha"/> ]     -->
  
  <ComProps :item="borracha" :preco="precoBorracha"/>
  <DataBinding/>
  <ComDadosReativosNaoPrimitivos/>
  <ComDadosReativosPrimitivos/>
  <ComDados/>
  <PrimeiroComponente/>
</template>


<style scoped>
</style>
