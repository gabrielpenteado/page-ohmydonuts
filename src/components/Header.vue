<script setup lang="ts">
const navigation = [
  { name: "Features", href: "#main-feature" },
  { name: "Technologies", href: "#technologies" },
  { name: "Contact", href: "#contact" },
];
</script>

<template>
  <div class="fixed inset-x-0 top-0 z-50 bg-white/80 backdrop-blur-sm">
    <nav
      class="flex items-center justify-center p-6 lg:px-8"
      aria-label="Global"
    >
      <div class="flex lg:flex-1 lg:ml-4">
        <a href="#" class="-m-1.5 p-1.5">
          <!-- <span class="text-2xl font-bold text-primary-600">Oh My Donuts</span> -->
          <img width="150" src="/logo.png" alt="logo" />
        </a>
      </div>
      <div class="hidden lg:flex lg:gap-x-12 lg:mr-4">
        <a
          v-for="item in navigation"
          :key="item.name"
          :href="item.href"
          class="text-base font-semibold leading-6 text-gray-900 hover:text-primary-600 transition-colors"
          >{{ item.name }}</a
        >
      </div>
      <!-- <div class="lg:flex lg:flex-1 lg:justify-end">
        <img class="w-24" src="/donut.png" alt="donut" />
      </div> -->
    </nav>
  </div>
</template>
