<script setup>
import {ref} from "vue";
import Content from './components/Content.vue'
import ColorBar from './components/ColorBar.vue'

const color = ref('#FFFFFF');
</script>

<template>
    <div class="content">
        <div class="zoom-out">
            <ColorBar @set-color="color = $event" />
            <Content :color="color" />
        </div>
    </div>
</template>
