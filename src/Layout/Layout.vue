<script setup>
import NavBar from "@/Layout/NavBar.vue";
import Footer from "@/Layout/Footer.vue";
</script>

<template>
  <NavBar/>
  <main>
    <slot/>
  </main>
  <Footer/>
</template>
