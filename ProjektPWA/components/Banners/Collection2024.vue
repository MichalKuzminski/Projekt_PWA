<template>
  <div class="banner-container">
    <div class="banner-container_content">
      <p>KOLEKCJA 2024 / MODOWE INSPIRACJE</p>
      <h1>CLICK FASHION</h1>
      <p>Ręcznie robione ubrania, naturalne materiały, polska marka</p>
      <a>WIĘCEJ</a>
    </div>
  </div>
</template>

<script>

export default {};
</script>

<style lang="scss" scoped>
@import '@/globalStyles.scss';

.banner-container {
  width: 100%;
  min-height: 650px;
  background-image: url('https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/p/r/projekt_bez_nazwy_1_.png');
  background-size: cover;
  background-position: 0 -60px;
  font-family: $second-font;

  &_content{
    max-width: 1140px;
  }
}

</style>
