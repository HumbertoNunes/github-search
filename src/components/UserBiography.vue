<script setup>
import { defineProps } from 'vue'

defineProps(['bio'])
</script>

<template>
    <div class="text-left text-gray-400 max-w-max">
        {{ bio ?? 'This profile has no bio'}}
    </div>
</template>