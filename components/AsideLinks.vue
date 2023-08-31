<template>
  <ul>
    <li v-for="el in nav">
    <ULink :to="el._path">{{ el.title }}</ULink>
    <AsideLinks v-if="el.children" :nav="el.children" />
    </li>
  </ul>
</template>

<script setup lang="ts">
const props = defineProps<{
  nav: any
}>()
</script>
