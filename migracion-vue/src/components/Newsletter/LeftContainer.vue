<template>
    <div class="text-center md:text-left">
      <TexNewsletter />
      <InputNewsletter />
    </div>
  </template>
  
  <script>  
    import TexNewsletter from './TexNewsletter.vue';
    import InputNewsletter from './InputNewsletter.vue';
  
  export default {
    components: {
      TexNewsletter,
      InputNewsletter
    }
  };
  </script>
  
  <style scoped>
  /* Tailwind CSS maneja la mayoría de los estilos */
  </style>