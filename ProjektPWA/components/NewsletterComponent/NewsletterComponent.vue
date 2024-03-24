<template>
  <div class="newsletter-wrapper">
    <div class="line"></div>
    <div class="title">Newsletter</div>
    <div class="newsletter-info">Nie przegap okazji, dołącz do naszego newslettera.</div>
    <div class="inputs-wrapper">
        <div class="input-group">
            <input type="text" placeholder="Podaj swój adres Email">
            <button>
                <span>ZAPISZ SIĘ! </span>
                <Icon class="icon" name="oi:arrow-right" />
            </button>
        </div>
        <div class="checkbox-group">
            <input class="checkbox" type="checkbox" name="rules">
            <label class="checkbox-label" for="rules">Zapoznałem/am się z polityką prywatności</label>
        </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
@import '@/globalStyles.scss';

.newsletter-wrapper {
    position: relative;
    background-color: $newsletter-background-color;
    color: $black;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-block: 80px;
    font-family: $merriweather-font;

    .line {
        position: absolute;
        top: -25px;
        left: 50%;
        height: 50px;
        border-left: 1px solid rgba(0, 0, 0, 0.76);
    }

    .title {
        font-size: 48px;
        font-weight: 600;
        margin-bottom: 13px;
        letter-spacing: 0px;
    }

    .newsletter-info {
        font-family: $merriweather-font;
        font-size: 12px;
        margin-bottom: 28px;
        font-weight: 300;
        letter-spacing: 0;
        color: $grey;
    }

    .input-group, .checkbox-group {
        display: flex;
    }

    .input-group {
        input {
            height: 48px;
            background-color: $white;
            border: 1px solid $inputs-border-color;
            border-right: none;
            padding-left: 14px;
            width: 367px;
            font-weight: 300;

            &:active, &:focus, &:focus-visible {
                outline: none;
            }
            
            &:focus {
                box-shadow: 0px 0px 10px $newsletter-button-color;
            }

            &::placeholder {
                font-size: 13px;
            }
        }

        button {
            min-width: 190px;
            padding: 3px 20px 0;
            background-color: $newsletter-button-color;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
            color: $white;
            font-size: 11px;
            transition: all 0.2s;
            
            span {
                font-family: $global-font;
                font-weight: 700;
                letter-spacing: 1.8px;
            }

            .icon {
                transform: scale(1.4);
                margin-right: 8px;
            }

            &:hover {
                background-color: rgba($newsletter-button-color, .9);
                .icon {

                margin-right: 4px;
                }
            }
        }
    }

    .checkbox-group {
        margin-top: 10px;
        align-items: flex-end;

        input.checkbox {
            margin-right: 10px;
            width: 20px;
            height: 20px;
        }

        label.checkbox-label {
            font-size: 10.5px;
            letter-spacing: .7px;
            font-family: $global-font;
        }
    }
}
</style>