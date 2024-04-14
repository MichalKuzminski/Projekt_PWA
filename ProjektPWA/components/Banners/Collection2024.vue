<template>
  <div class="banner-container">
    <div class="banner-container_socials">
      <p>SOCIAL MEDIA</p>
      <div class="banner-container_socials_icons">
        <Icon class="icon" name="jam:facebook-square" />
        <Icon class="icon" name="mdi:instagram" />
      </div>
    </div>
    <div class="banner-container_content">
      <p class="collection">KOLEKCJA 2024 / MODOWE INSPIRACJE</p>
      <h1>CLICK FASHION</h1>
      <p class="desc">
        Ręcznie robione ubrania, naturalne materiały, polska marka
      </p>
      <button>
        <span>WIĘCEJ</span><Icon class="icon" name="oi:arrow-right" />
      </button>
    </div>
    <div class="banner-container_indent"></div>
    <img
      src="https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/p/r/projekt_bez_nazwy_1_.png"
      alt="baner-image"
    />
  </div>
</template>

<style lang="scss" scoped>
@import '@/globalStyles.scss';
.banner-container {
  position: relative;
  width: 100%;
  min-height: 650px;
  background: linear-gradient(rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)),
    url('https://clickfashion.pl/media/idea07_contenttypes/contenttypeentity/image/p/r/projekt_bez_nazwy_1_.png');
  background-size: cover;
  background-position: 0 -60px;
  font-family: $global-font;
  font-weight: 500;
  display: flex;
  align-items: flex-start;
  justify-content: flex-end;

  img {
    position: absolute;
    object-fit: cover;
    bottom: 0;
    right: 20%;
    width: 240px;
    height: 160px;
  }

  &_socials {
    background-color: $white;
    @include flex-center;
    flex-direction: column;
    justify-content: space-evenly;
    gap: 20px;
    width: 70px;
    height: 328px;

    &_icons {
      display: flex;
      flex-direction: column;
      justify-content: space-around;
      gap: 25px;

      .icon {
        font-size: 25px;
        cursor: pointer;
      }
    }

    p {
      color: $grey;
      font-weight: 200;
      font-size: 1rem;
      writing-mode: vertical-rl;
      text-orientation: mixed;
    }
  }

  &_content {
    position: absolute;
    right: 65%;
    top: 20%;
    color: $white;
    max-width: 530px;

    .collection {
      letter-spacing: 2px;
      font-size: 0.75rem;
      font-weight: 800;
    }

    h1 {
      font-size: 5rem;
      font-weight: 600;
      white-space: break-spaces;
      line-height: 6rem;
    }
    .desc {
      font-family: $merriweather-font;
      font-weight: 200;
      font-size: 14px;
      letter-spacing: 0.7px;
      max-width: 270px;
      margin-bottom: 5%;
    }

    button {
      width: 190px;
      @include flex-center;
      justify-content: space-around;
      margin-right: 50px;
      letter-spacing: 1px;
      padding: 9px 0;
      background-color: black;
      border: 1px solid black;
      font-weight: 600;
      font-size: 0.9rem;
      transition: all 0.3s ease;

      &:hover {
        color: black;
        background-color: $white;
      }
    }
  }

  &_indent {
    left: 0;
    bottom: 0;
    position: absolute;
    width: 500px;
    height: 112px;
    background-color: $white;
  }
}
</style>
