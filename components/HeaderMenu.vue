<template>
  <div class="flex flex-row">
    <UButton v-for="dir in navigation.filter(el => el.children)" :label="dir.title" :to="dir._path" variant="ghost" size="lg" />
  </div>
</template>

<script lang="ts" setup>
const {
  // Global references
  globals,
  navigation,
  surround,
  page,
  // Computed properties from `page` key
  excerpt,
  toc,
  type,
  layout,
  // Computed properties from `surround` key
  next,
  prev
} = useContent()
</script>



<style>

</style>
