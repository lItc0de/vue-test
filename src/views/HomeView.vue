<script setup>
const recipes = [
  {
    title: "Apple pie",
    description: "Just like your Mums",
    author: "Joe Bloggs",
    dateCreated: new Date(2022, 1, 1),
  },
  {
    title: "Bratwurst",
    description: "The best in Kreuzberg",
    author: "Hans Solo",
    dateCreated: new Date(2021, 8, 31),
  },
];
</script>

<template>
  <main>
    <h2>Recipe list</h2>
    <ul>
      <li v-for="recipe in recipes" :key="recipe.title">
        <p>{{ recipe.title }}</p>
        <p>{{ recipe.description }}</p>
        <p>Created by {{ recipe.author }} on {{ recipe.dateCreated }}</p>
      </li>
    </ul>
  </main>
</template>
