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
                <a href="#">
                  <span class="sr-only">Workflow</span>
                  <img class="h-8 w-auto sm:h-10" src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg" alt="" />
                </a>
                <div class="flex -mr-2 items-center md:hidden">
                  <PopoverButton class="rounded-md bg-gray-50 p-2 text-gray-400 inline-flex items-center justify-center hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-inset focus:ring-2 focus:ring-indigo-500">
                    <span class="sr-only">Open main menu</span>
                    <MenuIcon class="h-6 w-6" aria-hidden="true" />
                  </PopoverButton>
                </div>
              </div>
            </div>
            <div class="hidden md:flex md:space-x-10">
              <a v-for="item in navigation" :key="item.name" :href="item.href" class="font-medium text-gray-500 hover:text-gray-900">{{ item.name }}</a>
            </div>
            <div class="hidden md:flex md:inset-y-0 md:right-0 md:absolute md:items-center md:justify-end">
              <span class="rounded-md shadow inline-flex">
                <a href="#" class="bg-white border border-transparent rounded-md font-medium text-base py-2 px-4 text-indigo-600 inline-flex items-center hover:bg-gray-50">
                  Home
                </a>
              </span>
            </div>
          </nav>
        </div>

        <transition enter-active-class="duration-150 ease-out" enter-from-class="opacity-0 scale-95" enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in" leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
          <PopoverPanel focus class="p-2 transform origin-top-right inset-x-0 transition top-0 z-10 absolute md:hidden">
            <div class="bg-white rounded-lg shadow-md ring-black ring-1 ring-opacity-5 overflow-hidden">
              <div class="flex px-5 pt-4 items-center justify-between">
                <div>
                  <img class="h-8 w-auto" src="https://tailwindui.com/img/logos/workflow-mark-indigo-600.svg" alt="" />
                </div>
                <div class="-mr-2">
                  <PopoverButton class="bg-white rounded-md p-2 text-gray-400 inline-flex items-center justify-center hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-inset focus:ring-2 focus:ring-indigo-500">
                    <span class="sr-only">Close menu</span>
                    <XIcon class="h-6 w-6" aria-hidden="true" />
                  </PopoverButton>
                </div>
              </div>
              <div class="px-2 pt-2 pb-3">
                <a v-for="item in navigation" :key="item.name" :href="item.href" class="rounded-md font-medium text-base py-2 px-3 text-gray-700 block hover:bg-gray-50 hover:text-gray-900">{{ item.name }}</a>
              </div>
              <a href="#" class="font-medium bg-gray-50 text-center w-full py-3 px-5 text-indigo-600 block hover:bg-gray-100">
                Log in
              </a>
            </div>
          </PopoverPanel>
        </transition>
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
              <a :href="href" class="border border-transparent rounded-md flex font-medium bg-indigo-600 text-base text-white w-full py-3 px-8 items-center justify-center md:text-lg md:py-4 md:px-10 hover:bg-indigo-700">
                {{ btn }}
              </a>
            </div>
            <div class="rounded-md shadow mt-3 sm:mt-0 sm:ml-3">
              <a :href="href2" class="bg-white border border-transparent rounded-md flex font-medium text-base w-full py-3 px-8 text-indigo-600 items-center justify-center md:text-lg md:py-4 md:px-10 hover:bg-gray-50">
                {{ btn2 }}
              </a>
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
  { name: 'Product', href: '#' },
]

const title = "The Future"
const title2 = "Is Now"
const subtitle = "This is a page all about the future and the dreams we have for the life that we want to build"
const btn = "Our Home"
const href ="https://www.domain.com.au/2-3d-may-street-scarborough-wa-6019-2017337860"
const btn2 = "Our Escape"
const href2 = "https://www.carsales.com.au/cars/details/2021-ford-ranger-raptor-px-mkiii-auto-4x4-my21-25-double-cab/OAG-AD-20103606/?Cr=14"
</script>