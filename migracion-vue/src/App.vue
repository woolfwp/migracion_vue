<template>
  <div>
    <h1>Hola, Vue está funcionando 🚀</h1>
    <Products />
    <RegresiveCount />
  </div>
</template>

<script setup>
import Products from './components/ProductsSection.vue';
import RegresiveCount from './components/RegresiveCount.vue';
</script>

<style>
h1 {
  color: blue;
}
</style>
