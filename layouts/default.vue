<template>
  <header class="border border-gray-800 bg-gray-200 dark:bg-slate-900">
    <div>
      <ul class="flex gap-8 p-4">
        <li>
          <NuxtLink to="/">Main Page</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About Page</NuxtLink>
        </li>
      </ul>
    </div>
  </header>
  <slot />
</template>

<script lang="ts" setup>
const colorMode = useColorMode()
console.log(colorMode.preference)
colorMode.preference = 'dark'
</script>

<style>
body {
  @apply bg-white dark:bg-slate-900 text-slate-700 dark:text-slate-400
}

a {
  @apply dark:hover:text-slate-300 focus:text-sky-400
}
</style>
