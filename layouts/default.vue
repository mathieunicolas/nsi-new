<template>
  <Header />
  <div class="grid grid-cols-10">
  <AsideMenu class="col-span-2" />
  <main class="col-span-8 p-8">
    <slot />
  </main>
  </div>
</template>

<script lang="ts" setup>

</script>



<style>

</style>
