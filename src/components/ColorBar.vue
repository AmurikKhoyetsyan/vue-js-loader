<template>
    <div class="row">
        <div
            v-for="(color, index) in colors"
            :key="index"
            class="parent-color"
        >
            <div
                class="color"
                :style="{ '--bg': color }"
                @click="$emit('set-color', color)"
            ></div>
        </div>
    </div>
</template>

<style scoped>
#app .parent-color {
    padding-left: 0.5rem;
    padding-right: 0.5rem;
}

#app .parent-color .color {
    width: 50px;
    height: 50px;
    cursor: pointer;
    background-color: var(--bg);
    border-radius: 50%;
}
</style>

<script setup>
const colors = [
    '#FFFFFF',
    '#ef3535',
    '#5c2ceb',
    '#69f759',
    '#ef8905',
    '#03a9f4',
    '#795548',
    '#e91e63',
    '#009688'
];

defineEmits(['set-color']);
</script>
