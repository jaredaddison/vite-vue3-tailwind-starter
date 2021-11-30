<template>
  <div class="mx-auto max-w-7xl py-10 sm:px-6 lg:px-8 ">
  <ul role="list" class="grid gap-x-4 gap-y-8 grid-cols-2 sm:gap-x-6 sm:grid-cols-3 lg:grid-cols-4 xl:gap-x-8">
    <li v-for="file in files" :key="file.source" class="relative">
      <div class="rounded-lg bg-gray-100 w-full group block overflow-hidden aspect-w-10 aspect-h-7 focus-within:ring-2 focus-within:ring-offset-2 focus-within:ring-offset-gray-100 focus-within:ring-indigo-500">
        <img :src="file.source" alt="" class="object-cover pointer-events-none group-hover:opacity-75" />
        <button type="button" class="inset-0 absolute focus:outline-none">
          <span class="sr-only">View details for {{ file.title }}</span>
        </button>
      </div>
      <p class="font-medium mt-2 text-sm text-gray-900 block truncate pointer-events-none">{{ file.title }}</p>
    </li>
  </ul>
  </div>
</template>

<script setup>
const files = [
  {
    title: 'Ford Ranger Raptop',
    source: '../public/images/raptor.png',
  },
]
</script>