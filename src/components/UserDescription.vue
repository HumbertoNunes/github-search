<script setup>
import { defineProps } from 'vue'

defineProps(['name', 'login', 'url', 'created_at'])

function format(date) {
	const created_at = new Date(date)
	return `Joined ${created_at.getDate()} ${created_at.toLocaleDateString('en', {month: 'short'})} ${created_at.getFullYear()}`
}
</script>

<template>
	<div class="flex items-center space-x-6 lg:relative">
		<img class="rounded-full w-20 h-20 bg-gray-300" :src="url" alt="">
		<div class="flex items-start flex-col text-lg">
			<span class="font-bold lg:text-2xl" :class="{'opacity-30': !name}">{{ name ?? login }}</span>
			<span class="text-gray-400 hidden lg:inline lg:absolute lg:top-51 lg:right-1">{{ format(created_at) }}</span>
			<span class="text-blue-400">@{{ login }}</span>
			<span class="text-gray-400 lg:hidden">{{ format(created_at) }}</span>
		</div>
	</div>
</template>