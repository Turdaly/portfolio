<template>
  <section class="">
    <h1>About</h1>
  </section>
</template>

<script setup lang="ts">
useSeoMeta({
  title: 'About Page',
  description: '[description]',
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
