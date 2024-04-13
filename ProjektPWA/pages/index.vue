<template>
            <BannersCollection2024 />
        <div class="clothes">
            <BannersTopBestsellers style="padding: 0 !important" />
            <div v-if="clothesData.length" class="clothes">
                <ClothesTile v-for="(cl, idx) in clothesData" :key="idx" :imageSrc="cl.img" :type="cl.type"
                    :color="cl.color" :price="cl.price" />
            </div>
            <div v-else>
                <h1>Wystąpił problem podczas wczytywania listy ubrań :(</h1>
            </div>
        </div>
</template>


<script lang="ts">
import { defineComponent, onMounted, ref } from 'vue'
import axios from 'axios'

export default defineComponent({
    setup() {

        interface IClothes {
            id: string,
            type: string,
            color: string,
            price: number,
            img: string
        }

        const clothesData = ref<IClothes[]>([])

        onMounted(async () => {
            clothesData.value = await (await axios.get('http://localhost:3001/clothes')).data
        })

        return {
            clothesData
        }

    },
})
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