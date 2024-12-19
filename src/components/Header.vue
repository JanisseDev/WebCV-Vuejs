<script setup>
import { inject } from 'vue'

const phone = inject('phone');
const mail = inject('mail');
const colorless = inject('colorless');
</script>

<template>
    <div class="root" :class="{'root-colorless': colorless}">
        <div class="left">
            <h1 class="font-title">Clément JANISSET</h1>
            <h1 class="font-subtitle">DÉVELOPPEUR FRONTEND</h1>
        </div>
        <div class="right font-info">
            <h1>42000 Saint-Etienne, France</h1>
            <h1>Permis B</h1>
            <h1>30 ans</h1>
            <br>
            <h1>{{phone}}</h1>
            <h1>{{mail}}</h1>
        </div>
    </div>
    <div v-if="!colorless" class="wave-mask"></div>
    <svg v-if="colorless" class="wave-mask-colorless" xmlns="http://www.w3.org/2000/svg">
        <path d="M0 38L21.5 39.3C43 40.7 86 43.3 128.8 39.7C171.7 36 214.3 26 257.2 20.3C300 14.7 343 13.3 385.8 16.7C428.7 20 471.3 28 514.2 32.8C557 37.7 600 39.3 642.8 37.8C685.7 36.3 728.3 31.7 771.2 26.8C814 22 857 17 878.5 14.5L900 12L900"
        fill="none" stroke="#dcdcdc" stroke-width="2px" stroke-linecap="round"></path>
    </svg>
</template>

<style scoped>
* {
    --wave-top-offset: 0px;
    --wave-height: 50px;
}

.root {
    display: flex;
    justify-content: space-between;
    color: white;
    padding-top: 20px;
    padding-left: 30px;
    padding-right: 30px;
    padding-bottom: calc(var(--wave-top-offset) + var(--wave-height));
    margin-bottom: calc(0px - var(--wave-height));
    flex: 0;
    background-image: radial-gradient(circle at 67% 83%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 1%, transparent 1%, transparent 5%, transparent 5%, transparent 100%), radial-gradient(circle at 24% 80%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 27%, transparent 27%, transparent 63%, transparent 63%, transparent 100%), radial-gradient(circle at 23% 5%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 26%, transparent 26%, transparent 82%, transparent 82%, transparent 100%), radial-gradient(circle at 21% 11%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 35%, transparent 35%, transparent 45%, transparent 45%, transparent 100%), radial-gradient(circle at 10% 11%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 21%, transparent 21%, transparent 81%, transparent 81%, transparent 100%), radial-gradient(circle at 19% 61%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 20%, transparent 20%, transparent 61%, transparent 61%, transparent 100%), radial-gradient(circle at 13% 77%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 63%, transparent 63%, transparent 72%, transparent 72%, transparent 100%), radial-gradient(circle at 30% 93%, hsla(317, 0%, 96%, 0.05) 0%, hsla(317, 0%, 96%, 0.05) 33%, transparent 33%, transparent 82%, transparent 82%, transparent 100%), linear-gradient(90deg, rgb(22, 176, 207), rgb(103, 7, 215));
}

.root-colorless {
    color: black;
    background-image: none;
}

.wave-mask {
    background: white;
    clip-path: path("M0 38L21.5 39.3C43 40.7 86 43.3 128.8 39.7C171.7 36 214.3 26 257.2 20.3C300 14.7 343 13.3 385.8 16.7C428.7 20 471.3 28 514.2 32.8C557 37.7 600 39.3 642.8 37.8C685.7 36.3 728.3 31.7 771.2 26.8C814 22 857 17 878.5 14.5L900 12L900 51L878.5 51C857 51 814 51 771.2 51C728.3 51 685.7 51 642.8 51C600 51 557 51 514.2 51C471.3 51 428.7 51 385.8 51C343 51 300 51 257.2 51C214.3 51 171.7 51 128.8 51C86 51 43 51 21.5 51L0 51Z");
    height: var(--wave-height);
    z-index: 10;
    padding-bottom: 1px; /* Magic value: Avoid pixel fighting */
}

.wave-mask-colorless {
    height: var(--wave-height);
}

.left {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    gap: 20px;
}

.right {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
}

.font-title {
    font-weight: 700;
    font-size: 2rem;
    letter-spacing: 0.2rem;
}

.font-subtitle {
    font-weight: 300;
    font-size: 1rem;
    letter-spacing: 0.05rem;
}

.font-info * {
    font-weight: 300;
    font-size: 0.8rem;
}
</style>