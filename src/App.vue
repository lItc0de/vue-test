<script setup>
import { RouterView } from "vue-router";

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

function createRecipe(recipe) {
  recipes.push(recipe)
}
</script>

<template>
  <div class="layout">
    <RouterView :recipes="recipes" :create-recipe="createRecipe" />
  </div>
</template>
<style>
  .layout {
    width: 800px;
    margin: 8px auto;
  }
</style>
