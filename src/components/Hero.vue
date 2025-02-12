<script setup lang="ts"></script>

<template>
  <div class="relative isolate pt-14">
    <div
      class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
    >
      <div
        class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-primary-200 to-primary-400 opacity-20 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"
      ></div>
    </div>

    <div class="py-24 sm:py-32">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl text-center">
          <h1
            class="text-4xl pb-2 font-bold tracking-tight text-primary-500 sm:text-6xl"
          >
            Sweet Success
          </h1>
          <span class="text-3xl font-semibold tracking-tight text-gray-900">
            Starts Here</span
          >
          <p class="mt-6 text-lg leading-8 text-gray-600">
            Run your donut shop smoothly with our easy-to-use solution.
          </p>
          <div class="mt-10 flex items-center justify-center gap-x-6">
            <a
              href="https://oh-my-donuts.netlify.app/"
              target="_blank"
              rel="noopener noreferrer"
              class="btn-primary"
            >
              Try Demo
            </a>
            <a
              href="https://www.youtube.com/watch?v=1vZzvyr_ZsU"
              target="_blank"
              rel="noopener noreferrer"
              class="btn-secondary"
            >
              Watch Teaser
            </a>
            <a
              href="https://github.com/gabrielpenteado/oh-my-donuts"
              target="_blank"
              rel="noopener noreferrer"
              class="btn-secondary"
            >
              Source Code
            </a>
          </div>
        </div>
        <div class="mt-16 flex justify-center">
          <img
            class="rounded-2xl max-w-xs lg:max-w-4xl shadow-2xl shadow-gray-700"
            src="/screenshot.webp"
            alt="screenshot"
          />
        </div>
      </div>
    </div>
  </div>
</template>
