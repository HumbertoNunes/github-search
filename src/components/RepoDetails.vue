<script setup>
import { defineProps } from 'vue'

const props = defineProps(['repos', 'followers', 'following'])
const items = ['Repos', 'Followers', 'Following']

</script>

<template>
	<div class="flex rounded-lg py-4 bg-blue-50 justify-around md:px-6">
		<div v-for="item in items" :key="item" class="flex flex-col">
			<span class="text-gray-400 font-semibold">{{ item }}</span>
			<span class="font-bold">{{ props[item.toLowerCase()] }}</span>
		</div>
	</div>
</template>