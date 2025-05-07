<template>
  <div class="home-page">
    <h1>Add New Todos</h1>
    <form @submit.prevent="">
      <input
        v-model="newTodoText"
        type="text"
        placeholder="Enter your todo"
        aria-label="New todo text"
      />
      <input type="submit" value="Add Todo" />
    </form>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const newTodoText = ref('')
</script>

<style scoped lang="scss">
.home-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

h1 {
  margin-bottom: 24px;
  color: #333;
}

form {
  display: flex;
  gap: 10px;
  width: 100%;
  max-width: 500px;
  input[type='text'] {
    flex-grow: 1;
    padding: 10px 15px;
    font-size: 1rem;
    border: 1px solid #ccc;
    border-radius: 4px;

    &:focus {
      outline: none;
      border-color: #007bff;
      box-shadow: 0 0 0 0.2rem rgba(0, 123, 255, 0.25);
    }
  }

  input[type='submit'] {
    padding: 10px 20px;
    font-size: 1rem;
    background-color: rgb(24, 120, 72);
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.2s ease-in-out;

    &:hover {
      background-color: rgb(20, 100, 60);
    }

    &:active {
      background-color: rgb(16, 80, 48);
    }
  }
}
</style>
