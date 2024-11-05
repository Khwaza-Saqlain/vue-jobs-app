<script setup>
import { defineProps } from 'vue';

defineProps({
    cardColor: {
        type: String,
        default: "bg-gray-100"
    }
})
</script>

<template>
    <div :class="`${cardColor} p-6 rounded-lg shadow-md`">
        <slot></slot>
    </div>
</template>