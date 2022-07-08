<template>
  <div class="rounded">
    <header>
      <nav>
        <h1
          class="bg-gradient-to-r from-cyan-300 to-cyan-400 text-center text-lg text-white font-bold p-2"
        >
          ACTIVITIES
        </h1>
      </nav>
      <SearchField />
    </header>
    <main class="p-2 flex flex-col">
      <a
        class="border border-dashed border-cyan-400 rounded-3xl text-cyan-400 p-2 text-center active:bg-cyan-100"
        >+ Add New</a
      >
      <TodoItem />
      <TodoItem />
    </main>
  </div>
</template>

<script setup lang="ts">
import SearchField from "./components/SearchField.vue";
import TodoItem from "./components/TodoItem.vue";
</script>
