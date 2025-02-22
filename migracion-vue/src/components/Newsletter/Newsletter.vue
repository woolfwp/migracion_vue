<template>
    <section class="bg-gray-900 text-white py-10 px-6 rounded-lg shadow-md">
      <div class="container mx-auto flex flex-col md:flex-row items-center justify-between">
        <LeftContainer />
        <SocialMediaIcons />
      </div>
    </section>
  </template>
  
  <script>
  import LeftContainer from '@/components/Newsletter/LeftContainer.vue';
  import SocialMediaIcons from '@/components/Newsletter/SocialMediaIcons.vue';
  
  export default {
    components: {
      LeftContainer,
      SocialMediaIcons
    }
  };
  </script>
  
  <style scoped>
  /* Tailwind CSS maneja la mayoría de los estilos */
  </style>
  