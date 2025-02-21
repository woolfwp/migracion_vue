<template>
  <section id="products" class="py-12 bg-gray-100">
    <div class="container mx-auto px-6 lg:px-12">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
        <!-- Confidential Cloud -->
        <div>
          <h2 class="text-3xl font-bold text-gray-800">Confidential Cloud</h2>
          <p class="mt-4 text-gray-600">
            Asegura la privacidad y seguridad de tus datos en la nube con cifrado avanzado y acceso controlado.
          </p>
          <button class="mt-6 bg-blue-600 text-white px-6 py-2 rounded-lg shadow-md hover:bg-blue-700">
            Más información
          </button>
        </div>
        <div>
          <img :src="confidentialCloud" alt="Confidential Cloud" class="rounded-lg shadow-lg">
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center mt-12">
        <!-- Safe Private Data Sharing -->
        <div>
          <h2 class="text-3xl font-bold text-gray-800">Safe Private Data Sharing</h2>
          <p class="mt-4 text-gray-600">
            Comparte datos de manera segura sin comprometer la privacidad, utilizando tecnologías avanzadas de cifrado.
          </p>
          <button class="mt-6 bg-green-600 text-white px-6 py-2 rounded-lg shadow-md hover:bg-green-700">
            Más información
          </button>
        </div>
        <div>
          <img :src="safePrivateData" alt="Safe Private Data Sharing" class="rounded-lg shadow-lg">
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center mt-12">
        <!-- Zero Knowledge Proof -->
        <div>
          <h2 class="text-3xl font-bold text-gray-800">Zero Knowledge Proof</h2>
          <p class="mt-4 text-gray-600">
            Verifica información sin revelar datos sensibles, con tecnología de prueba de conocimiento cero.
          </p>
          <button class="mt-6 bg-purple-600 text-white px-6 py-2 rounded-lg shadow-md hover:bg-purple-700">
            Más información
          </button>
        </div>
        <div>
          <img :src="zeroKnowledgeProof" alt="Zero Knowledge Proof" class="rounded-lg shadow-lg">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import confidentialCloud from '@/assets/images/confidential-cloud.png';
import safePrivateData from '@/assets/images/safe-private-data-sharing.png';
import zeroKnowledgeProof from '@/assets/images/zero-knowledge-proof.png';

export default {
  name: "ProductsSection",
  data() {
    return {
      confidentialCloud,
      safePrivateData,
      zeroKnowledgeProof
    };
  }
};
</script>

<style>
/* Estilos personalizados si son necesarios */
</style>
