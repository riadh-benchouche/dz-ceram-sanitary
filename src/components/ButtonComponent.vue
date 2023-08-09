<script setup>
import {defineProps} from "vue";

defineProps({
  title: {
    type: String,
    required: true
  },
  color: {
    type: String,
    default: "bg-primary"
  },
  textColor: {
    type: String,
    default: "text-white"
  },
  size: {
    type: String,
    default: "text-sm"
  },
  link: {
    type: String,
    default: "#"
  },
  otherProps: {
    type: String,
    default: ""
  }
})
</script>

<template>
  <a :href="link"
     :class="[`bg-${color} text-${size} hover:bg-${color}/90 text-${textColor} ${otherProps}`,'rounded-md px-3.5 py-2.5 font-semibold shadow-sm']">
    {{ title }}
  </a>
</template>
