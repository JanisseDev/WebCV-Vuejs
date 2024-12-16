<script setup>
defineProps({
    title: {
        type: String,
        required: true,
    },
    direction: {
        type: String,
        required: false,
    },
})
</script>

<template>
    <div class="main">
        <div class="title-container">
            <div class="line"></div>
            <h2 class="font-title">{{ title }}</h2>
            <div class="line"></div>
        </div>
        <slot></slot>
    </div>
</template>

<style scoped>
.main {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    justify-content: center;
    gap: calc(20px);
    flex: 0;
}

.title-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
}

.line {
    background-color: #dcdcdc;
    height: 4px;
    flex: 1;
}

.font-title {
    font-weight: 400;
    font-size: 1.2rem;
    letter-spacing: 0.15rem;
}
</style>