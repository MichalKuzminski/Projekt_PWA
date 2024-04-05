<template>
  <footer>
    <section class="">
      <div class="grid-containter">
        <div class="links-box">
          <h3 class="links-box-title">Poradnik zakupowy</h3>
          <ul>
            <li class="links-box-link">
              <a href="#!">Metody płatności</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Formy dostawy</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Reklamacje</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Zwrot, wymiana</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Kontakt</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Testowy Link</a>
            </li>
          </ul>
        </div>

        <div class="links-box">
          <h3 class="links-box-title">Zasady i regulaminy</h3>
          <ul>
            <li class="links-box-link">
              <a href="#!">Regulamin sklepu</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Regulamin karty stałego klienta</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Regulamin karty podarunkowej</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Saldo karty podarunkowej</a>
            </li>
          </ul>
        </div>

        <div class="links-box">
          <h3 class="links-box-title">O nas</h3>
          <ul>
            <li class="links-box-link">
              <a href="#!">Regulamin sklepu</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Regulamin karty stałego klienta</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Regulamin karty podarunkowej</a>
            </li>
            <li class="links-box-link">
              <a href="#!">Saldo karty podarunkowej</a>
            </li>
          </ul>
        </div>

        <div class="links-box">
          <Icon class="icon" name="jam:facebook-square" />

          <Icon class="icon" name="devicon:twitter" />

          <Icon class="icon" name="mdi:instagram" />
        </div>
      </div>
    </section>
  </footer>
</template>

<script setup></script>

<style lang="scss" scoped>
@import '@/globalStyles.scss';

.grid-containter {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  width: 1600px;
}

.links-box-title {
  letter-spacing: 0.6px;
  line-height: 1.5;
  font-weight: 700;

  text-transform: uppercase;
  margin-bottom: 20px;
  margin-top: 0;
  text-align: left;
}

.links-box {
  flex-direction: column;
  text-align: left;
  margin-bottom: 49px;
  padding-left: 60px;
  padding-right: 60px;
}

.links-box-link {
  line-height: 1.9;
  margin: 0 0 10px;
  letter-spacing: 0.3px;
  color: #000;
}
ul {
  list-style: none;
}

.icon {
  font-size: 30px;
  margin-right: 20px;
}

footer {
  box-sizing: border-box;
  margin-left: auto;
  margin-right: auto;
  max-width: 1600px;
  padding-left: 40px;
  padding-right: 40px;
  width: auto;
}

section {
  font-family: $global-font;
  padding-top: 62px;
  font-size: 12px;
}
</style>
