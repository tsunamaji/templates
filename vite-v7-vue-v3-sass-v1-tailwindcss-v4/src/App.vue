<script setup lang="ts">
import Counter from './components/Counter.vue'
</script>

<template>
  <div class="max-w-2xl my-4 mx-auto bg-stone-800/80 rounded-lg shadow-2xl shadow-tsunamaji">
    <a href="https://rozsazoltan.vercel.app/ecosystem" target="_blank" class="flex gap-4 items-center">
      <img src="/tsunamaji.svg" class="logo" alt="Tsunamaji logo" />
      <h1 class="text-2xl font-bold text-stone-500">Tsunamaji</h1>
    </a>

    <Counter />
  </div>
</template>

<style lang="scss" scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;

  &:hover {
    filter: drop-shadow(0 0 2em #646cffaa);

    &.vue {
      filter: drop-shadow(0 0 2em #42b883aa);
    }
  }
}
</style>

<style lang="css" scoped>
@reference "#tailwind.css";

.logo {
  border-color: var(--color-stone-500); /* or @apply border-stone-500; */
  @apply border-r-4 border-b-4 rounded-br-lg;
}
</style>
