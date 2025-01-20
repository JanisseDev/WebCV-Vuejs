<script setup>
import { inject } from 'vue'

defineProps({
    teamSize: {
        type: String,
        required: false,
    },
    tags: {
        type: Array,
        required: true,
    },
})

const colorless = inject('colorless');
</script>

<template>
    <div class="main">
        <div class="row">
            <p class="font-subtitle team-icon" v-if="teamSize == 1">Solo</p>
            <p class="font-subtitle team-icon" v-if="teamSize && teamSize != 1">Équipe: {{ teamSize }}</p>
            <p class="font-subtitle" v-if="teamSize">-</p>
            <p class="tag" :class="{'tag-colorless': colorless}" v-for="(tag) in tags">{{ tag }}</p>
        </div>
        <slot></slot>
    </div>
</template>

<style scoped>
/* LAYOUT */
.main {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    flex: 1;
}

.row {
    display: flex;
    align-items: center;
    gap: 5px;
    margin-bottom: 3px;
}

.tag {
    font-weight: 300;
    font-size: 0.7rem;
    letter-spacing: 0rem;
    background: linear-gradient(194deg, rgb(54 182 210) 0%, rgb(94 141 215) 100%);
    color: white;
    padding: 2px 8px;
    border-radius: 10vh;
}

.tag-colorless {
    color: black;
    background: none;
    border-color: black;
    border: 1px solid;
    padding: 1px 7px;
}

.team-icon::before {
    content: '';
    background-image: url('@/assets/users.svg');
    background-repeat: no-repeat;
    background-position: center center;
    display: inline-block;
    padding-right: 3px;
    vertical-align: text-bottom;
    background-size: contain;
    width: 0.8rem;
    height: 0.8rem;
    font-weight: 900;
}

/* FONTS */
.font-subtitle {
    font-weight: 300;
    font-size: 0.8rem;
    font-style: italic;
    letter-spacing: 0rem;
}
</style>