<template>
    <div class="page">
        <slot></slot>
    </div>
</template>

<style scoped>
.page {
    background-color: white;
    width: 840px; /*  210px * 4  */
    height: 1188px; /*  297px * 4  */
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    flex: none;
}
</style>