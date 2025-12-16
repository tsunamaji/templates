<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}

function decrement() {
  count.value--
}
</script>

<template>
  <div class="flex flex-col items-center justify-center p-6 space-y-4">
    <h2 class="text-2xl font-bold">Counter: {{ count }}</h2>
    <div class="flex space-x-4 *:cursor-pointer">
      <button class="btn" @click="decrement">-</button>
      <button class="btn" @click="increment">+</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.btn {
  background-color: var(--color-tsunamaji); /* Since TailwindCSS is also loaded, you have access to its variables */
  &:hover {
    background-color: #2563eb;
  }

  &:active {
    background-color: #1d4ed8;
  }
}
</style>

<style lang="css" scoped>
@reference "#tailwind.css";

.btn {
  @apply px-4 py-2 rounded font-semibold text-white transition-colors;
}
</style>

