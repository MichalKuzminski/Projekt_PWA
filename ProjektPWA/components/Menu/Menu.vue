<script setup lang="ts">
import { ref } from 'vue'

const isSearchOpen = ref(false)

const searchClickHandler = () => {
  isSearchOpen.value = !isSearchOpen.value
};
</script>
 
<template>
    <div class="container flex place-content-between max-w-screen-xl p-4 mx-auto">
            <NuxtLink to="/">
              <img src="https://clickfashion.pl/media/logo/websites/1/clickfashion-logo.png" title="" alt="Click Fashion" width="170" height="43" style="">   
            </NuxtLink>
        <div class="flex gap-4 items-center">
            <select>
              <option>
                PL
              </option>
              <option>
                EN
              </option>
            </select>
            <div class="flex">
              
              <div v-if="isSearchOpen" class="search-box">
                SZUKAJ W SKLEPIE...
              </div>
              <img src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/search.svg" @click="searchClickHandler()" alt="Open Box" style="cursor: pointer;" />
            </div>
            <NuxtLink to="/konto">
              <img src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/account.svg"/>
            </NuxtLink>
            <NuxtLink to="/ulubione">
              <img src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/heart.svg"/>
            </NuxtLink>
            <NuxtLink to="/wozek">
              <img class="border-l-2 pl-4" src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/cart.svg"/>
            </NuxtLink>
        </div>
    </div>
    <nav class="bg-white border-gray-200 dark:bg-gray-900">
  <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
    <div class="hidden w-full md:block md:w-auto">
      <ul class="font-light flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
        <li>
          <NuxtLink to="/" class="animation block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">SKLEP</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/kolekcja-zimowa" class="animation block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">KOLEKCJA ZIMOWA</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/stylizacje-codzienne" class="animation block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">STYLIZACJE CODZIENNE</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/kolekcja-swiateczna" class="animation block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">KOLEKCJA ŚWIĄTECZNA</NuxtLink>
        </li>
        <li>
          <NuxtLink to="wyprzedaz" class="animation block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">WYPRZEDAŻ</NuxtLink>
        </li>
        <li>
          <NuxtLink to="nowosci" class="animation block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">NOWOŚCI</NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>
 
<style lang="scss" scoped>
@import '@/globalStyles.scss';
 
.text {
  font-family: $merriweather-font;
}
 
 
 
/* Underline styles */
.animation {
  display: block;
  position: relative;
  padding: 0.2em 0;
}
 
/* Fade in */
.animation::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 0.1em;
  background-color: black;
  opacity: 0;
  transition: opacity 500ms, transform 500ms;
}
 
.animation:hover::after,
.animation:focus::after {
  opacity: 1;
  transform: translate3d(0, 0.2em, 0);
}
 
/* Slide in */
li .animation {
  overflow: hidden;
}
 
li .animation::after {
  opacity: 1;
  transform: translate3d(-100%, 0, 0);
}
 
li .animation:hover::after,
li .animation:focus::after{
  transform: translate3d(0, 0, 0);
}

.search-box {
  /* Your box styling goes here */
  border: 1px solid #ccc;
  padding: 10px;
}

</style>