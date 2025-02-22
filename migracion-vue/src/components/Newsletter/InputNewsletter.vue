<template>
    <form @submit.prevent="submitForm" class="flex flex-col md:flex-row gap-4">
      <input v-model="email" type="email" placeholder="Tu correo electrónico"
        class="px-4 py-2 rounded-lg border border-gray-300 focus:ring-2 focus:ring-blue-500 w-full md:w-auto">
      <button type="submit"
        class="bg-blue-600 text-white px-6 py-2 rounded-lg shadow-md hover:bg-blue-700 transition">
        Suscribirse
      </button>
    </form>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const email = ref('');
  
      const submitForm = () => {
        if (!email.value.includes('@')) {
          alert('Por favor, introduce un correo válido.');
          return;
        }
        console.log('Correo enviado:', email.value);
        email.value = '';
      };
  
      return { email, submitForm };
    }
  };
  </script>
  
  <style scoped>
  /* Tailwind CSS maneja la mayoría de los estilos */
  </style>