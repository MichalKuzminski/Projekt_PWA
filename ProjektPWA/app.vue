<template>
  <div>
    <NuxtLayout>
      <NuxtPage/>
    </NuxtLayout>
  </div>
</template>
<script setup>
import { onMounted } from "vue";
  onMounted(() => {
    localStorage.setItem('nuxt-color-mode','light')
  })
</script>