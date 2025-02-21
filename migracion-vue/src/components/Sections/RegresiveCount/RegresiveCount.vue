<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const targetDate = new Date('2025-12-31T23:59:59').getTime();
const timeLeft = ref(getTimeLeft());

function getTimeLeft() {
  const now = new Date().getTime();
  const difference = targetDate - now;
  return {
    days: Math.floor(difference / (1000 * 60 * 60 * 24)),
    hours: Math.floor((difference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)),
    minutes: Math.floor((difference % (1000 * 60 * 60)) / (1000 * 60)),
    seconds: Math.floor((difference % (1000 * 60)) / 1000)
  };
}

let interval = null;

onMounted(() => {
  interval = setInterval(() => {
    timeLeft.value = getTimeLeft();
  }, 1000);
});

onUnmounted(() => {
  clearInterval(interval);
});
</script>

<template>
  <div class="flex flex-col items-center justify-center p-6 bg-gray-900 text-white rounded-2xl shadow-lg">
    <h2 class="text-2xl font-bold mb-4">Cuenta regresiva</h2>
    <div class="flex gap-4 text-center">
      <div class="p-4 bg-gray-800 rounded-xl">
        <span class="text-3xl font-semibold">{{ timeLeft.days }}</span>
        <div class="text-sm">Días</div>
      </div>
      <div class="p-4 bg-gray-800 rounded-xl">
        <span class="text-3xl font-semibold">{{ timeLeft.hours }}</span>
        <div class="text-sm">Horas</div>
      </div>
      <div class="p-4 bg-gray-800 rounded-xl">
        <span class="text-3xl font-semibold">{{ timeLeft.minutes }}</span>
        <div class="text-sm">Minutos</div>
      </div>
      <div class="p-4 bg-gray-800 rounded-xl">
        <span class="text-3xl font-semibold">{{ timeLeft.seconds }}</span>
        <div class="text-sm">Segundos</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* No se necesita un archivo CSS externo, todo está en Tailwind */
</style>
