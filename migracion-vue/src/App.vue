<template>
  <Navbar />
  <ProductsSection />
  <RegresiveCount />
</template>

<script>
import Navbar from './components/Navbar.vue';
import ProductsSection from './components/ProductsSection.vue';
import RegresiveCount from './components/RegresiveCount.vue';

export default {
  components: {
    Navbar,
    ProductsSection,
    RegresiveCount
  }
};
</script>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
