<script setup>
import { ref } from 'vue'
import AppHeader from './components/AppHeader'
import SearchBar from './components/SearchBar'
import UserProfile from './components/UserProfile'

let user = ref(null)

function load(data) {
  user.value = data
}
</script>

<template>
  <div class="w-11/12 mt-14 m-auto text-center min-w-min max-w-screen-sm space-y-8 transition-all delay-300 dark:text-white md:w-8/12 lg:w-7/12 font-mono">
    <AppHeader></AppHeader>
    <SearchBar @search="load"></SearchBar>
    <UserProfile :user="user"></UserProfile>
  </div>
</template>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
