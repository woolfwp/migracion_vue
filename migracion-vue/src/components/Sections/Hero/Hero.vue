<template>
    <section class="h-screen flex flex-col justify-center items-center text-center bg-gradient-to-b from-blue-500 to-blue-700 text-white">
      <h1 class="text-4xl md:text-6xl font-bold mb-4">Bienvenido a Verifiably</h1>
      <p class="text-lg md:text-xl max-w-2xl">La mejor plataforma para verificación de documentos de forma segura y rápida.</p>
      
      <div class="mt-6">
        <router-link to="/registro" class="bg-white text-blue-600 px-6 py-2 rounded-lg shadow-md hover:bg-gray-200">
          Regístrate Ahora
        </router-link>
      </div>
      
      <CountdownTimer class="mt-6" />
      
      <button @click="scrollToSection" class="mt-10 animate-bounce">
        <IconArrowDown class="w-8 h-8" />
      </button>
    </section>
  </template>
  
  <script>
  import { IconArrowDown } from 'lucide-vue-next';
  import CountdownTimer from '@/components/CountdownTimer.vue';
  
  export default {
    components: { IconArrowDown, CountdownTimer },
    setup() {
      const scrollToSection = () => {
        document.getElementById('next-section').scrollIntoView({ behavior: 'smooth' });
      };
      return { scrollToSection };
    }
  };
  </script>
  
  <style>
  /* Tailwind CSS maneja la mayoría de los estilos */
  </style>
  