<template>
    <div class="info-wrapper" v-if="!isClosed">
        <div class="content-wrapper">
            <slot></slot>
            <Icon @click="closeHeader" class="content-icon" name="ci:close-circle" color="white" />
        </div>
    </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

const isClosed = ref(false)

const closeHeader = () => {
    isClosed.value = true
}

</script>

<style lang="scss" scoped>
@import '@/globalStyles.scss';

.content-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    background-color: $header-info-background-color;
    padding-inline: $header-info-padding;
    height: $header-info-height;
    font-size: 11px;
    font-family: $global-font;
    font-weight: 600;
    gap: 3px;
    color: $white;

    .content-icon {
        position: absolute;
        right: $header-info-padding;
        transition: all 0.2s;
        font-size: 22px;

        &:hover {
            transform: scale(1.07);
        }
    }
}
</style>