<template>
  <footer class="overflow-hidden">
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
      <nav class="-mx-5 -my-2 flex flex-wrap justify-center">
        <div v-for="link in links" :key="link.title" class="px-5 py-2">
          <NuxtLink :to="link.path" class="text-base text-primary dark:text-text-secondary-dark">
            {{ link.title }}
          </NuxtLink>
        </div>
      </nav>

      <div class="mt-8 flex justify-center space-x-6">
        <a href="https://x.com/guillaumebriday" class="text-primary dark:text-text-secondary-dark">
          <span class="sr-only">X</span>
          <svg class="size-5" fill="currentColor" viewBox="0 0 512 512">
            <path
              fill-rule="evenodd"
              d="M389.2 48h70.6L305.6 224.2 487 464H345L233.7 318.6 106.5 464H35.8L200.7 275.5 26.8 48H172.4L272.9 180.9 389.2 48zM364.4 421.8h39.1L151.1 88h-42L364.4 421.8z"
              clip-rule="evenodd"
            />
          </svg>
        </a>

        <a href="https://github.com/stimulus-components" class="text-primary dark:text-text-secondary-dark">
          <span class="sr-only">GitHub</span>
          <GithubIcon />
        </a>
      </div>

      <p class="mt-8 text-center text-balance text-base text-text-secondary">
        &copy; {{ new Date().getFullYear() }} Stimulus Components. By
        <a href="https://guillaumebriday.fr" class="underline hover:no-underline" target="_blank">Guillaume Briday</a>.
      </p>
    </div>
  </footer>
</template>

<script setup>
import GithubIcon from "@/components/Icons/GithubIcon.vue"

const links = [
  { title: "Docs", path: "/docs" },
  { title: "Sponsors", path: "/sponsors" },
]
</script>
