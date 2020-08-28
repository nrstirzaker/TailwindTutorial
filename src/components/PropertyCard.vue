<template>
  <div>

    <div class="relative bg-red-500 pb-5/6 rounded-lg overflow-auto shadow-md">
      <img class="absolute top-0 h-full w-full object-cover" :src="property.imageUrl" :alt="property.imageAlt">
    </div>

    <div class="relative px-4 -mt-16">
      <div class="bg-white p-6 rounded-lg shadow-lg" >
        <div class="flex items-center">

        <span v-if="property.new"
              class="bg-teal-200 text-teal-800 text-xs px-2 rounded-full uppercase font-semibold tracking-wide mr-2">New</span>

          <div class="text-gray-600 text-xs uppercase font-semibold tracking-wide">
            {{property.beds}} beds &bull; {{property.baths}} baths
          </div>

        </div>

        <h4 class="mt-1 font-semibold text-lg leading-tight truncate">{{ property.title}}</h4>

        <div class="mt-1">
          {{property.formattedPrice}}
          <span class="text-gray-600 text-sm">/wk</span>
        </div>

        <div class="mt-4 flex items-center">

          <svg v-for="i in 5" :key="i" :class="i <= property.rating ? 'text-teal-500' : 'text-gray-400'" class="h-4 w-4 fill-current" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" >
            <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
          </svg>
          <span class="text-gray-600 text-sm">based on {{property.reviewCount}} reviews</span>
        </div>
      </div>
      </div>

  </div>

</template>

<script>
export default {
  props: ['property'],
  name: "PropertyCard"
}
</script>

<style scoped>

</style>