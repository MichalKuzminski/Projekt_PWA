<script setup>
</script>

<template>
    <div class="container flex flex-wrap max-w-screen-xl">
        <div class="items-center justify-between mx-auto p-4 ">
            <img src="https://clickfashion.pl/media/logo/websites/1/clickfashion-logo.png" title="" alt="Click Fashion" width="170" height="43" style="">   
        </div>
        <div class="flex flex-wra">
            <img src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/search.svg"/>
            <img src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/account.svg"/>
            <img src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/heart.svg"/>
            <img src="https://clickfashion.pl/static/version1709801068/frontend/Idea07/client-customization/en_US//images/icons/cart.svg"/>
            
        </div>
    </div>
    <nav class="bg-white border-gray-200 dark:bg-gray-900">
  <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
    <div class="hidden w-full md:block md:w-auto">
      <ul class="font-light flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
        <li>
          <NuxtLink to="/" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">SKLEP</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/kolekcja" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">KOLEKCJA ZIMOWA</NuxtLink>
        </li>
        <li>
          <NuxtLink to="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">STYLIZACJE CODZIENNE</NuxtLink>
        </li>
        <li>
          <NuxtLink to="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">KOLEKCJA ŚWIĄTECZNA</NuxtLink>
        </li>
        <li>
          <NuxtLink to="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">WYPRZEDAŻ</NuxtLink>
        </li>
        <li class="textbox">
          <NuxtLink to="#" class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent text">NOWOŚCI</NuxtLink>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>

<style lang="scss" scoped>
@import '@/globalStyles.scss';

.text {

    font-family: 'Schneidler Std Mediaeval Small Caps Light';

}



/* Underline styles */
a {
  display: block;
  position: relative;
  padding: 0.2em 0;
}

/* Fade in */
a::after {
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

a:hover::after,
a:focus::after {
  opacity: 1;
  transform: translate3d(0, 0.2em, 0);
}

/* Slide in */
li a {
  overflow: hidden;
}

li a::after {
  opacity: 1;
  transform: translate3d(-100%, 0, 0);
}

li a:hover::after,
li a:focus::after{
  transform: translate3d(0, 0, 0);
}

.toolbox{
    box-sizing: border-box;
    margin-left: auto;
    margin-right: auto;
    max-width: 1140px;
    padding-left: 40px;
    padding-right: 40px;
    width: auto;
}








</style>