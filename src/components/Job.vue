<script setup>
import { inject } from 'vue'

defineProps({
    title: {
        type: String,
        required: true,
    },
    startMonth: {
        type: String,
        required: false,
    },
    startYear: {
        type: String,
        required: false,
    },
    endMonth: {
        type: String,
        required: false,
    },
    endYear: {
        type: String,
        required: false,
    },
    places: {
        type: Array,
        required: false,
    },
    jobType: {
        type: String,
        required: false,
    },
    subtitle: {
        type: String,
        required: true,
    },
})

const showMonth = inject('showMonth');
const thickerText = inject('thickerText');
</script>

<template>
    <div class="main">
        <div class="left">
            <div class="date-div">
                <p class="font-date" v-if="startYear">{{ (showMonth && startMonth) ? startMonth+' ' : '' }}{{ startYear }}</p>
                <p class="font-date" v-if="startYear">-</p>
                <p class="font-date">{{ (showMonth && endMonth) ? endMonth+' ' : '' }} {{ endYear }}</p>
            </div>
            <p class="font-place" :class="{ 'font-place-thicker': thickerText }" v-for="(place) in places">{{ place }}</p>
        </div>
        <div class="right">
            <div class="row">
                <h3 class="font-title">{{ title }}</h3>
                <p class="font-subtitle">-</p>
                <p class="font-subtitle" v-if="jobType">{{ jobType }}</p>
                <p class="font-subtitle" v-if="jobType">-</p>
                <p class="font-subtitle">{{ subtitle }}</p>
            </div>
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
/* LAYOUT */
.main {
    display: flex;
    align-items: flex-start;
    justify-content: space-around;
    gap: 20px;
    break-inside: avoid;
}

.left {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    width: 80px;
}

.date-div {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 5px;
}

.right {
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

/* FONTS */
.font-date {
    font-weight: 400;
    font-size: 0.8rem;
    letter-spacing: 0rem;
    text-align: end;
}

.font-place {
    font-weight: 100;
    font-size: 0.7rem;
    letter-spacing: 0rem;
}

.font-place-thicker {
    font-weight: 300;
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