<script setup>
const colorMode = useColorMode()
const toast = useToast()

const isDark = computed({
  get () {
    return colorMode.value === 'dark'
  },
  set () {
    colorMode.preference = colorMode.value === 'dark' ? 'light' : 'dark'
  }
})
</script>

<template>
  <div class="header sticky top-0 z-50 w-full backdrop-blur flex-none border-b border-gray-900/10 dark:border-gray-50/[0.06] bg-white/75 dark:bg-gray-900/75">
  <div class="flex flex-row content-center space-x-4 > * + *">
    <span class="titre">Ma Prog'
    </span>
  </div>

  <HeaderMenu />
  <UButton
      :icon="isDark ? 'i-heroicons-moon-20-solid' : 'i-heroicons-sun-20-solid'"
      color="gray"
      variant="ghost"
      aria-label="Theme"
      @click="isDark = !isDark"
    />
  </div>
</template>

<style scoped>
.header {
  border-bottom: 1px solid lightgray;
  padding: 1rem;
  margin-bottom: 2rem;
  display: flex;
  flex-direction: row;
  justify-content: space-between; 
}

.titre {
  font-size: 2rem;
}

</style>