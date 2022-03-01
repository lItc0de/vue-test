<script setup>
const props = defineProps({
  recipes: Array
})
</script>

<template>
  <main>
    <h2>Recipe list</h2>
    <ul>
      <li v-for="recipe in props.recipes" :key="recipe.title">
        <p>{{ recipe.title }}</p>
        <p>{{ recipe.description }}</p>
        <p>Created by {{ recipe.author }} on {{ recipe.dateCreated }}</p>
      </li>
    </ul>
  </main>
</template>
