<template>
    <nav class="bg-white shadow-md fixed w-full z-50">
      <div class="container mx-auto px-4 py-3 flex justify-between items-center">
        <router-link to="/" class="text-2xl font-bold text-gray-800">Verifiably</router-link>
        
        <button @click="toggleMenu" class="md:hidden text-gray-800">
          <IconMenu />
        </button>
        
        <ul :class="{'hidden': !isOpen, 'block': isOpen}" class="md:flex space-x-6">
          <li v-for="link in navLinks" :key="link.name">
            <router-link :to="link.path" class="text-gray-600 hover:text-gray-800">
              {{ link.name }}
            </router-link>
          </li>
        </ul>
      </div>
    </nav>
  </template>
  
  <script>
  import { ref } from 'vue';
  import { IconMenu } from 'lucide-vue-next';
  
  export default {
    components: { IconMenu },
    setup() {
      const isOpen = ref(false);
      const navLinks = ref([
        { name: 'Inicio', path: '/' },
        { name: 'Productos', path: '/productos' },
        { name: 'Contacto', path: '/contacto' }
      ]);
      
      const toggleMenu = () => {
        isOpen.value = !isOpen.value;
      };
      
      return { isOpen, navLinks, toggleMenu };
    }
  };
  </script>
  
  <style>
  /* Tailwind maneja estilos directamente en clases */
  </style>
  