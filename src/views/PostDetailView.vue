<template>
  <div class="post-detail">
    This is a Post page
  </div>
  <p>display content of the post id of {{ $route.params.id }} here</p>
  <div>
    <button @click="showPostId" class="btn">show posts id</button>
  </div>
  <div>
    <button @click="redirect" class="btn">home</button>
  </div>
  <div>
    <button @click="goToFirstPost" class="btn">go to 1st post</button>
  </div>
  <p>
    <router-link to="/posts">back</router-link>
  </p>
</template>

<script setup>

import {useRoute, useRouter} from "vue-router";

const route = useRoute()
const router = useRouter()
const showPostId = () => {
  alert(`the id of this post ${route.params.id}`)
}
const redirect = () => {
  router.push({name: 'home'})
}
const goToFirstPost = () => {
  router.push({
    name: 'postDetail',
    params: {
      id: 'id1'
    }
  })
}
</script>

<style scoped>

</style>