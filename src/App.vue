<template>
  <div class="
    w-11/12 mt-14 m-auto text-center min-w-min max-w-screen-sm space-y-8 transition-all delay-300
    md:w-8/12
    lg:w-7/12
    font-mono
  ">
    <div class="flex justify-between">
      devfinder
      <div class="w-1/4 flex justify-around uppercase lg:w-1/6">
        light
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
        </svg>
      </div>
    </div>

    <!-- Search Bar-->
    <div class="flex items-center justify-between p-4 py-2 bg-white rounded-lg shadow-lg">
      <label for="search">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-blue-600" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
        </svg>
      </label>
      <input id="search" class="bg-transparent outline-none w-[69%] md:w-3/4" type="text" placeholder="Search GitHub username...">
      <button class="bg-blue-600 text-white font-semibold rounded-lg p-2">Search</button>
    </div>

    <!-- Profile Card -->
    <div class="bg-white rounded-lg shadow-lg p-6 space-y-4">
      <!-- Name Info -->
      <div class="flex items-center space-x-6 lg:relative">
        <div class="rounded-full w-20 h-20 bg-gray-300"></div>
        <div class="flex items-start flex-col text-lg">
          <span class="font-bold lg:text-2xl">The Octocat</span>
          <span class="text-gray-400 hidden lg:inline lg:absolute lg:top-51 lg:right-1">Joined 25 Jan 2011</span>
          <span class="text-blue-400">@octocat</span>
          <span class="text-gray-400 lg:hidden">Joined 25 Jan 2011</span>
        </div>
      </div>

      <div class="space-y-4 lg:pl-24">
        
      <!-- Bio -->
      <div class="text-left text-gray-500">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
      </div>

      <!-- Repo Info -->
      <div class="flex rounded-lg py-4 bg-blue-50 justify-around md:px-6">
        <div class="flex flex-col">
          <span class="text-gray-400 font-semibold">Repos</span>
          <span class="font-bold">8</span>
        </div>
        <div class="flex flex-col">
          <span class="text-gray-400 font-semibold">Followers</span>
          <span class="font-bold">3938</span>
        </div>
        <div class="flex flex-col">
          <span class="text-gray-400 font-semibold">Following</span>
          <span class="font-bold">9</span>
        </div>
      </div>

      <!-- Location Info -->
      <div class="space-y-2 md:flex md:space-x-20 md:space-y-0">
        <div class="space-y-2 md:flex md:flex-col">
          <div class="flex space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
            </svg>
            <span>San Francisco</span>
          </div>

          <div class="flex space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1" />
            </svg>
            <span>https://github.blog</span>
          </div>
        </div>
        
        <div class="space-y-2 md:flex md:flex-col">
          <div class="flex space-x-2 opacity-30">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
            <span>Not Available</span>
          </div>
          <div class="flex space-x-2">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
              <path stroke-linecap="round" stroke-linejoin="round" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
            </svg>
            <span>@github</span>
          </div>
        </div>
      </div>

      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
}
</script>

<style>
body {
  background-color: rgb(239 246 255);
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
