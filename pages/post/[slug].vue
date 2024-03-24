<template>
    <div class="max-w-3xl mx-auto min-h-screen my-12">
      <div v-if="post">
        <h1 class="text-2xl font-semibold mb-6">{{ post.title }}</h1>
        <!-- <ContentDoc :query=query></ContentDoc> -->
        <p> {{ route.path }} </p>
        <ContentDoc></ContentDoc>
        <div class="mt-8">
          <nuxt-link to="/" class="hover:underline">Back to blog</nuxt-link>
        </div>
      </div>
    </div>
  </template>
  
<script setup lang="ts">
const route = useRoute()
const post_name = route.params.slug
// const query = queryContent().where({'slug': post_name}).findOne()
const {data: post} = await useAsyncData('post', ()=> queryContent().where({'slug': post_name}).findOne())
// export default {
  //   })
  //   data() {
  //     return {
  //       post: null,
  //     }
  //   },
  //   async fetch() {
  //     this.post = (
  //       await this.$content()
  //         .where({ slug: this.$route.params.slug })
  //         .limit(1)
  //         .fetch()
  //     )?.[0]
  //   },
  // }
  </script>