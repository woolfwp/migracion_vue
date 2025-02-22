<template>
    <footer class="bg-gray-900 text-white py-8">
      <div class="container mx-auto px-6 lg:px-12">
        <div class="text-center mb-6">
          <img src="/images/verifiably-logo.png" alt="Verifiably" class="mx-auto w-64" />
          <p class="mt-2 text-gray-400">Email: <a href="mailto:contact@verifiably.com" class="text-blue-400">contact@verifiably.com</a></p>
          <p class="text-gray-400">Phone: <a href="tel:+12064865783" class="text-blue-400">+1 (206) 486 5783</a></p>
        </div>
  
        <div class="flex justify-between text-gray-400 text-sm border-t border-gray-700 pt-4">
          <p>{{ footerData.copywrite }}</p>
          <a href="https://www.linkedin.com/company/verifiably/about/" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-linkedin text-blue-400 text-xl"></i>
          </a>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  import footerData from '@/data/FooterData';
  
  export default {
    data() {
      return {
        footerData
      };
    }
  };
  </script>
  
  <style>
  /* Tailwind CSS maneja la mayoría de los estilos */
  </style>
  