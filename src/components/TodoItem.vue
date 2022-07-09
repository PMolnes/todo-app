<template>
  <div class="flex items-center border p-2 rounded-3xl gap-1">
    <div class="w-4 h-4 rounded-full" :class="getCategory(props.category)"></div>
    <label for="todo">{{ props.title }}</label>
    <input class="ml-auto rounded-full focus:ring-cyan-300 checked:bg-cyan-300" id="todo" type="checkbox" />
  </div>
</template>

<script setup lang="ts">

const categories = new Map() as Map<string, string>;
categories.set("work", "bg-yellow-300");
categories.set("home", "bg-blue-300");

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
  category: {
    type: String, 
    required: true,
  }
});

const getCategory = (category: string) => {
  return categories.get(category) || "bg-gray-300";
};
</script>
