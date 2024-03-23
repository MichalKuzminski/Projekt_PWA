<template>
    <div class="card" @mouseenter="blurred = true" @mouseout="blurred = false">
        <img :src="imageSrc" alt="Obrazek" :class="!blurred ? 'card-image' : 'card-image-blurred'">

        <div class="description-wrapper">
            <div class="card-description" v-if="!blurred">
                <b>
                    <p class="line1">{{ `${type} ` }}{{ color }}</p>
                </b>
                <p class="line2">Już od {{ price }},00 zł</p>
            </div>
            <div class="card-description" v-else>
                <p>Rozmiary dostępne wkrótce</p>
            </div>
        </div>
    </div>
</template>
<script lang="ts">
import { defineComponent, ref, watch } from 'vue'

export default defineComponent({
    props: {
        imageSrc: {
            type: String,
            required: true
        },
        type: {
            type: String,
            required: true
        },
        color: {
            type: String,
            required: true
        },
        price: {
            type: Number,
            required: true
        }
    },
    setup() {
        const blurred = ref(false)

        // watch(blurred, () => {
        //     console.log('blurred: ', blurred.value)
        // })
        return {
            blurred,
        }

    },
})
</script>

<style scoped>
.card {
    border: 1px solid #ccc;
    box-shadow: 5px 5px 5px 5px gray;
    overflow: hidden;
    width: 300px;
    color: black;
    margin: 2%
}

.description-wrapper {
    height: 100%;
}

.card-image {
    width: 100%;
    height: auto;
}

.card-image-blurred {
    width: 100%;
    height: auto;
    filter: blur(4px)
}

.card-description {
    padding: 10px;
}

.line1,
.line2 {
    margin: 0;
    line-height: 1.2;
}
</style>
