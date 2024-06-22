<script>
import { store } from '../store.js';

export default {
        data() {
    return {
        store
    }
}
}
</script>

<template>
    <div class="div-general">
        <div class="div-first" v-for="item in store.caratteri" :key="item.id">
            <div class="div-second">
                <img :src="item.card_images[0].image_url" alt="Card">
            
                <h3>
                    {{ item.name }}
                </h3>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use './style/partials/mixins.scss' as*;
    @use './style/partials/variabls.scss' as*;

    div.div-general {
        max-width: 1200px;
        background-color: #d48f38;
    }

    div.div-first{
        display: inline-block;
        max-width: 950px;
        margin: 0 auto;
        width: calc(100% / 6);
        vertical-align: top;
        margin: 1rem;
    }

        img{
            width: 100%;
        }

</style>