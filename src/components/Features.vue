<script setup lang="ts">
import { ClipboardDocumentListIcon } from "@heroicons/vue/24/outline";
</script>

<template>
  <div
    id="main-feature"
    class="sm:py-10 bg-gradient-to-b from-white to-primary-50"
  >
    <div class="mx-auto max-w-fit px-6 lg:px-8 text-center">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="section-title">Take Control of Your Donut Orders</h2>
      </div>
      <div class="mx-auto max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-none">
        <div
          class="feature-card rounded-lg border border-gray-200 bg-white p-6 shadow-md hover:shadow-xl transition-all duration-300 transform hover:border-primary-500"
        >
          <div class="flex items-center gap-x-3">
            <component
              :is="ClipboardDocumentListIcon"
              class="h-6 w-6 flex-none text-primary-600"
            />
            <h3 class="text-lg text-gray-600">
              Quickly manage all your donut orders, from when they’re placed to
              when they’re delivered.
            </h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
