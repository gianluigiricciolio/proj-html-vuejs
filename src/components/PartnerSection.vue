<script>
import BlackSubmit from './BlackSubmit.vue'
import GreenSubmit from './GreenSubmit.vue'

import { store } from '../store.js'

export default {
    name: 'PartnerSection',
    data() {
        return {
            store
        }
    },

    components: {
        BlackSubmit,
        GreenSubmit
    }
};

</script>

<template>
    <div class="main-container">
        <div class="submits d-flex justify-content-center">
            <BlackSubmit></BlackSubmit>
            <GreenSubmit></GreenSubmit>
        </div>
        <div class="container">
            <div class="partner-images d-flex justify-content-between align-items-center">
                <div v-for="partner in store.partners" class="partner-image">
                    <img :src="partner.img" alt="">
                </div>

            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../assets/scss/partials/_variables.scss' as *;

.main-container {
    width: 100%;
    background: linear-gradient(to top,
            $section-color 0%,
            $section-color 60%,
            white 60%,
            white 100%);
    padding: 200px 0 150px 0;

    .partner-images {
        margin-top: 150px;
    }
}
</style>