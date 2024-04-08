<template>
    <div>
        <!-- <NuxtWelcome /> -->
        <TopInfoComponent>
            <Icon name="ci:shopping-cart-02" />
            <div>
                PRODUKTY TWORZONE RĘCZNIE, WYSYŁKA MOŻE WYDŁUŻYĆ SIĘ DO 5 DNI
            </div>
        </TopInfoComponent>
        <Menu>
            
        </Menu>
        <slot/>

        <NewsletterComponent/>
        <BottomInfoComponent>
            <template #content-left>
                © 2023 CLICK FASHION. Wszelkie prawa zastrzeżone.
            </template>

            <template #content-right>
                Proudly made by grupa3pwa
            </template>
        </BottomInfoComponent>
    </div>
</template>
<script lang="ts">

</script>
<style scoped>

</style>