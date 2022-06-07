<script setup>
import { ref, defineEmits } from 'vue'
import axios from 'axios'

const name = ref()

const emit = defineEmits(['search'])

async function search() {
  if (name.value) {
      let user = await axios.get(`https://api.github.com/users/${name.value}`)
      .then(({data}) => data)

      emit('search', user)
  }
}
</script>

<template>
    <!-- Search Bar-->
    <form @submit.prevent="search" class="flex items-center justify-between p-4 py-2 bg-white rounded-lg shadow-lg dark:bg-slate-700">
        <label for="search">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
            </svg>
        </label>
        <input id="search" v-model="name" class="bg-transparent outline-none w-[69%] md:w-3/4 p-1 dark:placeholder:text-white" type="text" placeholder="Search GitHub username...">
        <button class="bg-blue-600 text-white font-semibold rounded-lg p-2">Search</button>
    </form>
</template>