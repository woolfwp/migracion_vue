<template>
  <div>
    <h1>Hola, Vue está funcionando 🚀</h1>
    <Products />
    <RegresiveCount />
    <Newsletter />
    <Team />
  </div>
</template>

<script setup>
import Newsletter from './components/Newsletter/Newsletter.vue';
import Products from './components/ProductsSection.vue';
import RegresiveCount from './components/RegresiveCount.vue';
import Team from '@/components/Team.vue'

</script>

<style>
h1 {
  color: blue;
}
</style>
