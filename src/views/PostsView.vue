<template>
  <div class="posts">
    <h1>Posts</h1>
    <ul>
      <li>
        <router-link to="/postDetail/id1">post 1</router-link>
        <router-link to="/postDetail/id2">post 2</router-link>
        <router-link to="/postDetail/id3">post 3</router-link>
      </li>
    </ul>
    <textarea v-autofocus/>
  </div>
</template>


<script setup>
import {vAutofocus} from "@/directives/vAutofocus";
</script>