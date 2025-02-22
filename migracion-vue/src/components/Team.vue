<template>
    <section class="bg-gray-100 py-12">
      <div class="container mx-auto px-6 lg:px-12 text-center">
        <h2 class="text-3xl font-bold text-gray-800 mb-6">Nuestro Equipo</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
          <div v-for="(member, index) in teamMembers" :key="index" class="bg-white p-6 rounded-lg shadow-md">
            <img :src="member.image" :alt="member.name" class="w-32 h-32 mx-auto rounded-full">
            <h3 class="text-lg font-semibold mt-4">{{ member.name }}</h3>
            <p class="text-gray-600">{{ member.role }}</p>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    setup() {
      const teamMembers = [
        { name: 'Juan Pérez', role: 'CEO', image: '/images/team1.jpg' },
        { name: 'María López', role: 'CTO', image: '/images/team2.jpg' },
        { name: 'Carlos García', role: 'Designer', image: '/images/team3.jpg' }
      ];
      return { teamMembers };
    }
  };
  </script>
  
  <style scoped>
  /* Tailwind CSS maneja la mayoría de los estilos */
  </style>