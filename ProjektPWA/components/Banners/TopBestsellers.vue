<template>
    <div class="container">
        <p class="title">Top Bestsellery</p>
        <p class="subtitle">najczęściej wybierane przez naszych klientów</p>
    </div>
</template>
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    setup() {

    },
})
</script>
<style scoped>
.container {
    width: 100%;
    height: 20%;
    background-color: white;
    text-align: center;
}

.title {
    font-family: 'Montserrat', sans-serif;
    font-size: 2.8rem;
    line-height: 1.2;
    color: black;
    margin: 15px;
    font-weight: 700;
    letter-spacing: 1.2px;
}

.subtitle {
    font-family: 'Merriweather', serif;
    font-size: 16px;
    line-height: 1.25;
    color: #676767;
    margin-top: 15px;

    margin-bottom: 40px;
}
</style>
