<script setup lang="ts">
import { RouterLink } from "vue-router";
</script>

<template>
  <div>
    <ul>
      <li>
        <RouterLink :to="{ name: 'landing-main' }"
          >la page avec une photo flatteuse</RouterLink
        >
      </li>
      <li>
        <RouterLink :to="{ name: 'experience' }"
          >La page avec des dates et des skills</RouterLink
        >
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
div {
  border-bottom: 1px solid black;
}
li {
  text-decoration: underline;
  color: blue;
}
ul {
  list-style-type: disc;
  display: block;
}
</style>
