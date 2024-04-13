<template>
  <div>
    <!-- <NuxtWelcome /> -->
    <TopInfoComponent>
      <Icon name="ci:shopping-cart-02" />
      <div>PRODUKTY TWORZONE RĘCZNIE, WYSYŁKA MOŻE WYDŁUŻYĆ SIĘ DO 5 DNI</div>
    </TopInfoComponent>
    <Menu></Menu>
    <slot />

    <InfoComponent />

    <NewsletterComponent />

    <Footer />

    <BottomInfoComponent>
      <template #content-left>
        © 2023 CLICK FASHION. Wszelkie prawa zastrzeżone.
      </template>

      <template #content-right> Proudly made by grupa3pwa </template>
    </BottomInfoComponent>
  </div>
</template>
<script lang="ts">
import { defineComponent, onMounted, ref } from 'vue';
import axios from 'axios';

export default defineComponent({
  setup() {
    interface IClothes {
      id: string;
      type: string;
      color: string;
      price: number;
      img: string;
    }

    const clothesData = ref<IClothes[]>([]);

    onMounted(async () => {
      clothesData.value = await (
        await axios.get('http://localhost:3001/clothes')
      ).data;
    });

    return {
      clothesData
    };
  }
});
</script>
<style scoped>
.clothes {
  display: flex;
  flex-wrap: wrap;
  background-color: $white;
  padding: 2%;
  color: $black;
  justify-content: center;
}
</style>
