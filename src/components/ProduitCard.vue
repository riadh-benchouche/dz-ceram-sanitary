<script setup>
import {defineProps} from "vue";

defineProps({
  name: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  image: {
    type: String,
    default: "https://picsum.photos/200/300"
  },
})

</script>

<template>
  <div>
    <img class="mx-auto h-48 w-48 md:h-56 md:w-56" :src="image" alt=""/>
    <h3 class="mt-6 text-base font-semibold leading-7 tracking-tight text-primary">{{ name }}</h3>
    <p class="text-sm leading-6 text-gray-400">{{ description }}</p>
  </div>
</template>
