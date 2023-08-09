<script setup>
import {
  ArrowRightIcon,
} from '@heroicons/vue/24/outline'
import ProduitCard from "@/components/ProduitCard.vue";

const products = [
  {
    name: 'Cuvette WC suspendu',
    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
    imageUrl:
        '/images/produits/produit1.png',
  },
  {
    name: 'Cuvette WC',
    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
    imageUrl:
        '/images/produits/produit2.png',
  },
  {
    name: 'Baignoire',
    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
    imageUrl:
        '/images/produits/produit3.png',
  },
  {
    name: 'lavabo centré',
    description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,',
    imageUrl:
        '/images/produits/produit4.png',
  },
]
</script>
<template>
  <div class="py-16 sm:py-20">
    <div class="mx-auto max-w-7xl px-6 text-center lg:px-8 z-20">
      <div class="flex justify-between items-center">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900">Nos produits</h2>
        <a href="#" class="leading-8 text-primary cursor-pointer">Voir tous
          <ArrowRightIcon class="inline-block w-5 h-5 ml-1"/>
        </a>
      </div>
      <ul role="list"
          class="mx-auto mt-8 grid max-w-7xl grid-cols-1 gap-6 sm:grid-cols-2 lg:mx-0 lg:max-w-none lg:grid-cols-4 lg:gap-8">
        <li v-for="(product,index) in products" :key="index"
            class="rounded-lg bg-white shadow-lg px-6 py-4 text-start">
          <produit-card :name="product.name" :description="product.description"
                        :image="product.imageUrl"/>
        </li>
      </ul>
    </div>
  </div>
</template>
