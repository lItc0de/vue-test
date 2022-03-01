<script setup>
import { useRouter } from "vue-router";
const router = useRouter();

const recipe = {
  title: "",
  description: "",
  author: "",
  createdDate: null,
};

const props = defineProps({
  createRecipe: Function,
});

function handleCreateRecipe() {
  props.createRecipe(recipe);
  router.push({ name: "home" });
}
</script>

<template>
  <main>
    <h2>Create Recipt</h2>
    <form @submit.prevent="handleCreateRecipe">
      <div class="form-group">
        <label for="title">Title</label>
        <input
          id="title"
          type="text"
          class="form-control"
          v-model="recipe.title"
        />
      </div>
      <div class="form-group">
        <label for="description">Description</label>
        <textarea
          id="description"
          class="form-control"
          v-model="recipe.description"
        ></textarea>
      </div>
      <div class="form-group">
        <label for="author">Author</label>
        <input
          id="author"
          type="text"
          class="form-control"
          v-model="recipe.author"
        />
      </div>
      <div class="form-group">
        <label for="created-at">Created At</label>
        <input
          id="created-at"
          type="date"
          class="form-control"
          v-model="recipe.createdDate"
        />
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </main>
</template>
