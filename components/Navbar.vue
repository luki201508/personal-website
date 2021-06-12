<template>
  <div
    class="
      w-full
      h-16
      bg-gray-50
      dark:bg-gray-800
      flex
      justify-center
      shadow-lg
      z-50
    "
  >
    <div class="w-3/4 flex justify-between items-center">
      <NuxtLink
        class="
          flex flex-col
          items-start
          font-mono font-semibold
          text-2xl text-gray-800
          dark:text-gray-300
          hover:text-gray-900
          dark:hover:text-gray-200
          transition
          duration-75
          leading-none
        "
        to="/"
      >
        <div>LUCAS</div>
        <div>GALIPOLO</div>
      </NuxtLink>
      <div class="flex items-center space-x-4">
        <NuxtLink
          v-for="{ name, href } in links"
          :key="name"
          :to="href"
          class="
            font-semibold
            text-gray-800
            dark:text-gray-300
            hover:text-gray-900
            dark:hover:text-gray-200
            hover:underline
          "
        >
          {{ name }}
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      links: [
        {
          name: 'Proyectos',
          href: '/work',
        },
        {
          name: 'Sobre mí',
          href: '/about',
        },
        {
          name: 'Cursos',
          href: '/courses',
        },
        {
          name: 'Contacto',
          href: '/contact',
        },
      ],
    }
  },
})
</script>
