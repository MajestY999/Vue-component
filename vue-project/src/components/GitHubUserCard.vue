<template>
  <div class="ui card">
    <div class="image">
      <img :src="user.avatar_url">
    </div>
    <div class="content">
      <a :href="`https://github.com/${username}`" class="header">{{ user.name }}</a>
      <div class="meta">
        <span class="date">Joined in {{ user.created_at }}</span>
      </div>
      <div class="description">
        {{ user.bio }}
      </div>
    </div>
    <div class="extra content">
      <a :href="`https://github.com/${username}?tab=followers`">
        <i class="user icon"></i>
        {{ user.followers }} Friends
      </a>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import axios from 'axios'


const props = defineProps(['username'])

const user = ref({})

onMounted(async () => {
 
  const res = await axios.get(`https://api.github.com/users/${props.username}`)
  user.value = res.data
})
</script>