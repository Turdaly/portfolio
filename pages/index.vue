<template>
  <section class="">
    <div>
      <h1>
        Main page
      </h1>
    </div>
    <section v-if="pending">Loading ...</section>
    <section v-else-if="error">Something wrong ... Try again!</section>
    <section v-else="data">Data</section>
  </section>
</template>

<script lang="ts" setup>
const {error, pending, data} = await useFetch('https://jsonplaceholder.typicode.com/posts')

useSeoMeta({
  title: 'Main Page',
  description: 'This is main page',
})

useHead({
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.png'
    }
  ]
})
</script>
