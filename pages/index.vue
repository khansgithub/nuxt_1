<template lang="pug">

</template>
  
<script setup lang="ts">
import type { ParsedContent } from '@nuxt/content/types';

interface Post extends ParsedContent{
  description: string,
  slug: string
}

// generics syntax
// https://debbie.codes/blog/migrating-nuxt2-nuxt3/
const {data: posts} = await useAsyncData('posts', ()=> queryContent<Post>().find())

// console.log(await posts.find())
</script>