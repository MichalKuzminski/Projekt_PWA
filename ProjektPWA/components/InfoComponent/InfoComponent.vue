<template>
  <div class="info-component">
    <div class="info-box">
      <Icon class="icon" name="circum:discount-1" />
      <h2 class="heading">SKORZYSTAJ Z PROMOCJI</h2>
      <p class="text">
        Odwiedzając naszą stronę zawsze możesz liczyć na ciekawe promocje
      </p>
    </div>
    <div class="info-box">
      <Icon class="icon" name="circum:delivery-truck" />
      <h2 class="heading">WYSYŁKA</h2>
      <p class="text">
        Gwarantujemy wysyłkę w ciągu 24h od zaksięgowania płatności
      </p>
    </div>
    <div class="info-box">
      <Icon class="icon" name="circum:lock" />
      <h2 class="heading">BEZPIECZNE ZAKUPY</h2>
      <p class="text">
        Kupując w naszym sklepie masz gwarancję bezpiecznych zakupów i płatności
      </p>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style lang="scss" scoped>
@import '@/globalStyles.scss';

.info-component {
  display: flex;
  justify-content: center;
  background-color: $newsletter-background-color;
  padding: 82px 0 62px;
  font-family: $global-font;
  font-size: 15px;

  .info-box {
    width: 440px;
    display: flex;
    align-items: center;
    flex-direction: column;
    gap: 20px;
    padding: 0 50px;
    text-align: center;
  }

  .icon {
    font-size: 80px;
    color: $black;
  }

  .heading {
    font-weight: 600;
    letter-spacing: 1.86px;
  }

  .text {
    font-weight: 400;
    font-size: 13px;
  }

  @media (max-width: 1024px) {
    flex-wrap: wrap;

    .info-box {
      width: 380px;
    }
  }
}
</style>
