<template>
  <div>
    <h2>Home</h2>
    <NuxtLink to="/about"></NuxtLink>
  </div>
  <ul>
    <li v-for="user in users" :key="user.id">{{ user.name }}</li>
  </ul>
</template>

<script setup>
const users = await $fetch("https://jsonplaceholder.typicode.com/users");
</script>
