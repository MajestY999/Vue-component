<template>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/semantic-ui/2.4.1/semantic.min.css">

  <div id="app" class="ui container" style="margin-top: 20px;">
    <h1>GitHub Profiles</h1>
    
    <GithubUserCard 
      v-for="u in usernames" 
      :key="u" 
      :username="u" 
    />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import GithubUserCard from './components/GithubUserCard.vue'


const usernames = ref(['danielkellyio', 'hootlex', 'rahaug', 'akryum'])
</script>