<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="bg-white relative overflow-hidden">
    <div class="hidden sm:h-full sm:w-full sm:inset-y-0 sm:block sm:absolute" aria-hidden="true">
      <div class="h-full mx-auto max-w-7xl relative">
        <svg class="right-full transform translate-y-1/4 translate-x-1/4 absolute lg:translate-x-1/2" width="404" height="784" fill="none" viewBox="0 0 404 784">
          <defs>
            <pattern id="f210dbf6-a58d-4871-961e-36d5016a0f49" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#f210dbf6-a58d-4871-961e-36d5016a0f49)" />
        </svg>
        <svg class="left-full transform -translate-y-3/4 -translate-x-1/4 absolute md:-translate-y-1/2 lg:-translate-x-1/2" width="404" height="784" fill="none" viewBox="0 0 404 784">
          <defs>
            <pattern id="5d0dd344-b041-4d26-bec4-8d33ea57ec9b" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#5d0dd344-b041-4d26-bec4-8d33ea57ec9b)" />
        </svg>
      </div>
    </div>

    <div class="pt-6 pb-16 relative sm:pb-24">
      <Popover>
        <div class="mx-auto max-w-7xl px-4 sm:px-6">
          <nav class="flex relative items-center justify-between sm:h-10 md:justify-center" aria-label="Global">
            <div class="flex flex-1 items-center md:inset-y-0 md:left-0 md:absolute">
              <div class="flex w-full items-center justify-between md:w-auto">
                  <span class="sr-only">Workflow</span>
                  <img class="h-8 w-auto sm:h-10" src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg" alt="" />
              </div>
            </div>
            <div class="hidden md:flex md:inset-y-0 md:right-0 md:absolute md:items-center md:justify-end">
            </div>
          </nav>
        </div>
      </Popover>

      <main class="mx-auto mt-16 max-w-7xl px-4 sm:mt-24">
        <div class="text-center">
          <h1 class="font-extrabold tracking-tight text-4xl text-gray-900 sm:text-5xl md:text-6xl">
            <span class="block xl:inline">{{ title }}</span>
            {{ ' ' }}
            <span class="text-indigo-600 block xl:inline">{{ title2 }}</span>
          </h1>
          <p class="mx-auto max-w-md mt-3 text-base text-gray-500 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl">
            {{ subtitle }}
          </p>
          <div class="mx-auto max-w-md mt-5 sm:flex sm:justify-center md:mt-8">
            <div class="rounded-md shadow">
              <router-link to="/" class="border border-transparent rounded-md flex font-medium bg-indigo-600 text-base text-white w-full py-3 px-8 items-center justify-center md:text-lg md:py-4 md:px-10 hover:bg-indigo-700">
                {{ btn }}
              </router-link>
            </div>
            <div class="rounded-md shadow mt-3 sm:mt-0 sm:ml-3">
              <router-link to="/about" class="bg-white border border-transparent rounded-md flex font-medium text-base w-full py-3 px-8 text-indigo-600 items-center justify-center md:text-lg md:py-4 md:px-10 hover:bg-gray-50">
                {{ btn2 }}
              </router-link>
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>

<script setup>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { MenuIcon, XIcon } from '@heroicons/vue/outline'

const navigation = [
  { name: '', href: '#' },
]

const title = "The Future"
const title2 = "Is Now"
const subtitle = "This is a page all about the future and the dreams we have for the life that we want to build"
const btn = "Beach House"
const btn2 = "Ranger Raptor"
</script>