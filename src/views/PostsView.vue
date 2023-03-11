<template>
  <div class="posts">
    <h1>Posts</h1>
    <ul>
      <li v-for="post in posts" :key="post.id">
        <router-link :to="`/postDetail/${post.id}`">{{ post.title }}</router-link>
      </li>
    </ul>
    <textarea v-autofocus/>
  </div>
</template>


<script setup>
import {vAutofocus} from "@/directives/vAutofocus";
import {ref} from "vue";

const posts = ref([
  {id: 1, title: 'post1'},
  {id: 2, title: 'post2'},
  {id: 3, title: 'post3'},
])

</script>