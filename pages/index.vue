<template>
  <div>
    <h2>Home</h2>
    <slot />
  </div>

  <p v-if="loading">Loading...</p>
  <ul v-else>
    <li v-for="user in user2">{{ user.name }}</li>
  </ul>
</template>

<script setup>
const users = await $fetch("https://jsonplaceholder.typicode.com/users");
const { loading, data: user2 } = await useLazyFetch(
  "https://jsonplaceholder.typicode.com/users"
);
</script>
