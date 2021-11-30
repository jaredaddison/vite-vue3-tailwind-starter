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
    title: 'Living Area',
    source: 'https://rimh2.domainstatic.com.au/hDSNADPJiNaA7hErYCtbwXIH9MY=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_3_1_211019_064316-w1920-h1280',
  },
    {
    title: 'Kithcen',
    source: 'https://rimh2.domainstatic.com.au/24-t1y9Lglj40ow39T8fpYfvV8o=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_1_1_211019_064316-w1920-h1280',
  },
    {
    title: 'Balcony',
    source: 'https://rimh2.domainstatic.com.au/5BRQCvpYrRYd1FIbSUoBIzfP38c=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_7_1_211019_064316-w1920-h1280',
  },
  {
    title: 'The View',
    source: 'https://rimh2.domainstatic.com.au/5kJiNlIIsHvSA54-BbTHr5LRlUg=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_8_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Msater Bedroom',
    source: 'https://rimh2.domainstatic.com.au/ROIAwgbmprdZ_vfcv5r7pC57uAY=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_28_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Master Bathroom',
    source: 'https://rimh2.domainstatic.com.au/De8fMAzEGI5f3LdikbiIsLbuAGU=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_14_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Study / Entertaining',
    source: 'https://rimh2.domainstatic.com.au/_SIIwa412PYazJQkQgvze7ea6f8=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_17_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Baileys Bedroom',
    source: 'https://rimh2.domainstatic.com.au/arapdiTCZ4uxq2muqge6gSFbyKo=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_30_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Ground Floor AirBNB',
    source: 'https://rimh2.domainstatic.com.au/_LPMwqTaT3zD0Nu7uyFuSDradRw=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_11_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Ground Floor AirBNB',
    source: 'https://rimh2.domainstatic.com.au/PXG794SadJhZ2PekjIDJdvb4PT0=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_13_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Underground AirBNB',
    source: 'https://rimh2.domainstatic.com.au/pX2cn4z-4_XtwJDVVfrWfsRTUx0=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_23_1_211019_064316-w1920-h1280',
  },
  {
    title: 'Underground AirBNB Garden',
    source: 'https://rimh2.domainstatic.com.au/qrLiuX4TtlbI3ELiHQS84rVhoRY=/fit-in/1920x1080/filters:format(jpeg):quality(80):no_upscale()/2017337860_27_1_211019_064316-w1920-h1280',
  },
]
</script>