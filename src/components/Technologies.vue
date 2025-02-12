<script setup lang="ts">
const technologies = ["Vue", "Vuex", "Sass", "PostgreSQL"];
</script>

<template>
  <div
    id="technologies"
    class="pt-20 sm:pb-10 bg-gradient-to-b from-primary-50 to-white"
  >
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="section-title">Baked with modern technology</h2>
        <p class="section-description">
          Powerful technology keeps Oh My Donuts running smoothly, securely, and
          fast.
        </p>
      </div>
      <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
        <dl
          class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 lg:gap-8"
        >
          <div
            v-for="tech in technologies"
            :key="tech"
            class="tech-card rounded-lg border border-gray-200 bg-white p-4 shadow-md hover:shadow-xl transition-all duration-300 transform hover:scale-105 hover:border-primary-500"
          >
            <dt class="text-center text-lg font-medium text-gray-900">
              {{ tech }}
            </dt>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>
