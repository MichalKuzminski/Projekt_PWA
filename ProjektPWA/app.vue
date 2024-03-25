<template>
  <div>
    <NuxtLayout>

    </NuxtLayout>
  </div>
</template>
<script setup>
import { onMounted } from "vue";
  onMounted(() => {
    localStorage.setItem('nuxt-color-mode','light')
  })
</script>