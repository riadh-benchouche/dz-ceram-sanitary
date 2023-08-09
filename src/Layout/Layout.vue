<script setup>
import NavBar from "@/Layout/NavBar.vue";
import Footer from "@/Layout/Footer.vue";
</script>

<template>
  <div class="bg-white">
    <NavBar/>
    <main>
      <slot/>
    </main>
    <Footer/>
  </div>
</template>
