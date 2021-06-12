<template>
  <div
    class="
      fixed
      right-4
      bottom-4
      bg-gray-900
      dark:bg-gray-200
      text-white
      dark:text-gray-900
      flex
      justify-center
      items-center
      shadow-lg
      rounded-lg
      transition
      z-[100]
    "
  >
    <div class="flex items-center justify-center w-full">
      <label for="toggle" class="flex items-center cursor-pointer p-4">
        <div class="relative">
          <input
            id="toggle"
            v-model="darkMode"
            type="checkbox"
            class="sr-only"
          />
          <div
            class="block bg-gray-600 dark:bg-gray-400 w-14 h-8 rounded-full"
          ></div>
          <div
            class="
              dot
              absolute
              left-1
              top-1
              bg-white
              w-6
              h-6
              rounded-full
              transition
            "
          ></div>
        </div>
        <div class="ml-3 dark:text-gray-700 text-gray-400 font-medium">
          Modo {{ mode }}
          <span v-if="$colorMode.value === 'light'">
            <i class="fas fa-moon"></i>
          </span>
          <span v-else><i class="fas fa-sun"></i></span>
        </div>
      </label>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data() {
    return {
      darkMode: this.$colorMode.value === 'dark',
    }
  },
  computed: {
    mode() {
      return this.$colorMode.value === 'dark' ? 'claro' : 'oscuro'
    },
  },
  watch: {
    darkMode(value: boolean) {
      if (value) this.$colorMode.preference = 'dark'
      else this.$colorMode.preference = 'light'
    },
  },
})
</script>

<style scoped>
input:checked ~ .dot {
  transform: translateX(100%);
  @apply bg-gray-700;
}
</style>
