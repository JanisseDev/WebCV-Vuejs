<script setup>
defineProps({
    titles: {
        type: Array,
        required: true,
    },
    date: {
        type: String,
        required: true,
    },
    place: {
        type: String,
        required: true,
    },
})
</script>

<template>
    <div class="main">
        <h2 class="font-title" v-for="(title) in titles">{{ title }}</h2>
        <p class="font-subtitle">{{date}}</p>
        <p class="font-subtitle">{{place}}</p>
    </div>
</template>

<style scoped>
.main {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.font-title {
    font-weight: 400;
    font-size: 0.9rem;
    letter-spacing: 0.04rem;
}

.font-subtitle {
    font-weight: 300;
    font-size: 0.8rem;
    font-style: italic;
    letter-spacing: 0rem;
}
</style>