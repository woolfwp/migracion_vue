<template>
  <div class="flex space-x-4">
    <a v-for="(icon, index) in socialLinks" :key="index" :href="icon.link" target="_blank" rel="noopener noreferrer">
      <img :src="icon.src" :alt="icon.alt" class="w-8 h-8 hover:opacity-80 transition">
    </a>
  </div>
</template>

<script>
import LinkedInIcon from '@/assets/icons/LinkedIn.svg';
import DiscordIcon from '@/assets/icons/Discord.svg';
import TwitterIcon from '@/assets/icons/Twitter.svg';

export default {
  setup() {
    const socialLinks = [
      { src: LinkedInIcon, alt: 'LinkedIn', link: 'https://www.linkedin.com' },
      { src: DiscordIcon, alt: 'Discord', link: 'https://www.discord.com' },
      { src: TwitterIcon, alt: 'Twitter', link: 'https://www.twitter.com' }
    ];
    return { socialLinks };
  }
};
</script>

<style scoped>
/* Tailwind CSS maneja la mayoría de los estilos */
</style>
  