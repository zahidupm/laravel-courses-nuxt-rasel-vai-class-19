<template></template>

<script setup>
// const users = await $fetch("https://jsonplaceholder.typicode.com/users");
const { loading, data: user2 } = await useLazyFetch(
  "https://jsonplaceholder.typicode.com/users"
);
</script>
