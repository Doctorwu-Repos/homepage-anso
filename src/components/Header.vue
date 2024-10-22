<script setup lang="ts">
const route = useRoute()
const routes = [
  { path: '/home', label: '首页' },
  { path: '/contact-us', label: '联系我们' },
]
</script>

<template>
  <header class="w-full shadow-[#DCDCDC]" flex="~ justify-center items-center">
    <section class="h-[80px] w-[950px]" flex="~ justify-between items-center">
      <img src="$/logo.png" class="w-35 object-cover">
      <nav class="h-full flex gap-6">
        <a
          v-for="({ path, label }) in routes"
          :key="path"
          :href="path"
          class="min-w-20 p-2 pt-8 text-4"
          hover="text-[#1D73BB] bg-gray-100"
          :class="{ 'text-[#1D73BB] border-b-2 border-[#1D73BB]': route.path === path }"
        >
          {{ label }}
        </a>
      </nav>
    </section>
  </header>
</template>
