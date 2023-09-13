<script setup>
import Layout from "@/Layout/Layout.vue";

const timeline = [
  {
    name: 'Founded company',
    description:
        'Nihil aut nam. Dignissimos a pariatur et quos omnis. Aspernatur asperiores et dolorem dolorem optio voluptate repudiandae.',
    date: 'Aug 2021',
    dateTime: '2021-08',
  },
  {
    name: 'Secured $65m in funding',
    description:
        'Provident quia ut esse. Vero vel eos repudiandae aspernatur. Cumque minima impedit sapiente a architecto nihil.',
    date: 'Dec 2021',
    dateTime: '2021-12',
  },
  {
    name: 'Released beta',
    description:
        'Sunt perspiciatis incidunt. Non necessitatibus aliquid. Consequatur ut officiis earum eum quia facilis. Hic deleniti dolorem quia et.',
    date: 'Feb 2022',
    dateTime: '2022-02',
  },
  {
    name: 'Global launch of product',
    description:
        'Ut ipsa sint distinctio quod itaque nam qui. Possimus aut unde id architecto voluptatem hic aut pariatur velit.',
    date: 'Dec 2022',
    dateTime: '2022-12',
  },
]
</script>
<template>
  <Layout>
    <div class="relative isolate -z-10 overflow-hidden bg-gradient-to-b from-indigo-100/20 pt-14">
      <div
          class="absolute inset-y-0 right-1/2 -z-10 -mr-96 w-[200%] origin-top-right skew-x-[-30deg] bg-white shadow-xl shadow-indigo-600/10 ring-1 ring-indigo-50 sm:-mr-80 lg:-mr-96"
          aria-hidden="true"/>
      <div class="mx-auto max-w-7xl px-6 py-32 sm:py-40 lg:px-8">
        <div
            class="mx-auto max-w-2xl lg:mx-0 lg:grid lg:max-w-none lg:grid-cols-2 lg:gap-x-16 lg:gap-y-6 xl:grid-cols-1 xl:grid-rows-1 xl:gap-x-8">
          <h1 class="max-w-2xl text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl lg:col-span-2 xl:col-auto">
            À Propos de DZ Ceram Sanitary
          </h1>
          <div class="mt-6 max-w-xl lg:mt-0 xl:col-end-1 xl:row-start-1">
            <p class="text-lg leading-8 text-gray-600">Chez DZ Ceram Sanitary, nous sommes passionnés par la création
              d'espaces de vie exceptionnels en mettant l'accent sur la qualité, l'élégance et la fonctionnalité. Depuis
              [année de fondation], notre entreprise s'est taillée une réputation d'excellence dans le domaine de la
              céramique sanitaire, devenant une référence incontournable pour les projets de salle de bains de premier
              plan.</p>
          </div>
          <img
              src="https://images.unsplash.com/photo-1547895749-888a559fc2a7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1964&q=80"
              alt=""
              class="mt-10 aspect-[6/5] w-full max-w-lg rounded-2xl object-cover sm:mt-16 lg:mt-0 lg:max-w-none xl:row-span-2 xl:row-end-2 "/>
        </div>
      </div>
      <div class="absolute inset-x-0 bottom-0 -z-10 h-24 bg-gradient-to-t from-white sm:h-32"/>
    </div>

    <!-- Timeline section -->
    <div class="mx-auto -mt-8 max-w-7xl px-6 lg:px-8">
      <div class="mx-auto grid max-w-2xl grid-cols-1 gap-8 overflow-hidden lg:mx-0 lg:max-w-none lg:grid-cols-4">
        <div v-for="item in timeline" :key="item.name">
          <time :datetime="item.dateTime" class="flex items-center text-sm font-semibold leading-6 text-primary">
            <svg viewBox="0 0 4 4" class="mr-4 h-1 w-1 flex-none" aria-hidden="true">
              <circle cx="2" cy="2" r="2" fill="currentColor"/>
            </svg>
            {{ item.date }}
            <div
                class="absolute -ml-2 h-px w-screen -translate-x-full bg-gray-900/10 sm:-ml-4 lg:static lg:-mr-6 lg:ml-8 lg:w-auto lg:flex-auto lg:translate-x-0"
                aria-hidden="true"/>
          </time>
          <p class="mt-6 text-lg font-semibold leading-8 tracking-tight text-gray-900">{{ item.name }}</p>
          <p class="mt-1 text-base leading-7 text-gray-600">{{ item.description }}</p>
        </div>
      </div>
    </div>

    <!-- Logo cloud -->
    <div class="mx-auto mt-32 max-w-7xl sm:mt-40 sm:px-6 lg:px-8">
      <div
          class="relative isolate overflow-hidden bg-gray-900 px-6 py-24 text-center shadow-2xl sm:rounded-3xl sm:px-16">
        <h2 class="mx-auto max-w-2xl text-3xl font-bold tracking-tight text-white sm:text-4xl">Our customers love
          us</h2>
        <p class="mx-auto mt-6 max-w-xl text-lg leading-8 text-gray-300">Aliquip reprehenderit incididunt amet quis
          fugiat ut velit. Sit occaecat labore proident cillum in nisi adipisicing officia excepteur tempor
          deserunt.</p>
        <div
            class="mx-auto mt-20 grid max-w-lg grid-cols-4 items-center gap-x-8 gap-y-12 sm:max-w-xl sm:grid-cols-6 sm:gap-x-10 sm:gap-y-14 lg:max-w-4xl lg:grid-cols-5">
          <img class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
               src="https://tailwindui.com/img/logos/158x48/transistor-logo-white.svg" alt="Transistor" width="158"
               height="48"/>
          <img class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
               src="https://tailwindui.com/img/logos/158x48/reform-logo-white.svg" alt="Reform" width="158"
               height="48"/>
          <img class="col-span-2 max-h-12 w-full object-contain lg:col-span-1"
               src="https://tailwindui.com/img/logos/158x48/tuple-logo-white.svg" alt="Tuple" width="158" height="48"/>
          <img class="col-span-2 max-h-12 w-full object-contain sm:col-start-2 lg:col-span-1"
               src="https://tailwindui.com/img/logos/158x48/savvycal-logo-white.svg" alt="SavvyCal" width="158"
               height="48"/>
          <img class="col-span-2 col-start-2 max-h-12 w-full object-contain sm:col-start-auto lg:col-span-1"
               src="https://tailwindui.com/img/logos/158x48/statamic-logo-white.svg" alt="Statamic" width="158"
               height="48"/>
        </div>
        <div class="absolute -top-24 right-0 -z-10 transform-gpu blur-3xl" aria-hidden="true">
          <div class="aspect-[1404/767] w-[87.75rem] bg-gradient-to-r from-[#80caff] to-[#4f46e5] opacity-25"
               style="clip-path: polygon(73.6% 51.7%, 91.7% 11.8%, 100% 46.4%, 97.4% 82.2%, 92.5% 84.9%, 75.7% 64%, 55.3% 47.5%, 46.5% 49.4%, 45% 62.9%, 50.3% 87.2%, 21.3% 64.1%, 0.1% 100%, 5.4% 51.1%, 21.4% 63.9%, 58.9% 0.2%, 73.6% 51.7%)"/>
        </div>
      </div>
    </div>

    <!-- Content section -->
    <div class="mt-32 overflow-hidden sm:mt-40">
      <div class="mx-auto max-w-7xl px-6 lg:flex lg:px-8">
        <div
            class="mx-auto grid max-w-2xl grid-cols-1 gap-x-12 gap-y-16 lg:mx-0 lg:min-w-full lg:max-w-none lg:flex-none lg:gap-y-8">
          <div class="lg:col-end-1 lg:w-full lg:max-w-lg lg:pb-8">
            <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Notre Histoire</h2>
            <p class="mt-6 text-xl leading-8 text-gray-600">Fondée par [Nom du Fondateur] avec une vision de
              révolutionner l'industrie de la céramique sanitaire en [lieu de fondation], DZ Ceram Sanitary est devenue
              un acteur de premier plan grâce à son engagement envers la qualité, la durabilité et l'innovation. Depuis
              notre création, nous avons travaillé sans relâche pour offrir à nos clients des produits qui allient
              esthétique et utilité, tout en respectant les normes les plus strictes en matière de fabrication.</p>
          </div>
          <div class="flex flex-wrap items-start justify-end gap-6 sm:gap-8 lg:contents">
            <div class="w-0 flex-auto lg:ml-auto lg:w-auto lg:flex-none lg:self-end">
              <img
                  src="https://plus.unsplash.com/premium_photo-1661962444566-9ee99a462870?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80"
                  alt="" class="aspect-[7/5] w-[37rem] max-w-none rounded-2xl bg-gray-50 object-cover"/>
            </div>
            <div
                class="contents lg:col-span-2 lg:col-end-2 lg:ml-auto lg:flex lg:w-[37rem] lg:items-start lg:justify-end lg:gap-x-8">
              <div class="order-first flex w-64 flex-none justify-end self-end lg:w-auto">
                <img
                    src="https://plus.unsplash.com/premium_photo-1661963026516-5ecf0e65e1b3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80"
                    alt="" class="aspect-[4/3] w-[24rem] max-w-none flex-none rounded-2xl bg-gray-50 object-cover"/>
              </div>
              <div class="flex w-96 flex-auto justify-end lg:w-auto lg:flex-none">
                <img
                    src="https://images.unsplash.com/photo-1583911300103-0aaeff286030?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1932&q=80"
                    alt="" class="aspect-[7/5] w-[37rem] max-w-none flex-none rounded-2xl bg-gray-50 object-cover"/>
              </div>
              <div class="hidden sm:block sm:w-0 sm:flex-auto lg:w-auto lg:flex-none">
                <img
                    src="https://images.unsplash.com/photo-1565891741441-64926e441838?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80"
                    alt="" class="aspect-[4/3] w-[24rem] max-w-none rounded-2xl bg-gray-50 object-cover"/>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Stats -->
    <div class="mx-auto mt-32 max-w-7xl px-6 sm:mt-40 lg:px-8">
      <div class="mx-auto max-w-7xl lg:mx-0 flex flex-col md:flex-row justify-between space-x-0 md:space-x-20">
        <div>
          <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Notre Philosophie</h2>
          <p class="mt-6 text-base leading-7 text-gray-600">Chez DZ Ceram Sanitary, nous croyons en la puissance du
            design
            pour transformer les espaces de vie. Chaque produit que nous créons est le fruit d'une réflexion approfondie
            sur la manière dont il peut améliorer votre quotidien. Notre équipe de designers talentueux s'efforce de
            repousser les limites de la créativité tout en maintenant un engagement indéfectible envers la qualité et la
            durabilité.</p>
        </div>
        <div class="mt-8 md:mt-0">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Notre Engagement</h2>
          <p class="mt-6 text-base leading-7 text-gray-600">
            Nous sommes fiers de contribuer à la création de salles de bains qui sont à la fois des sanctuaires de
            détente
            et des exemples de sophistication. Notre engagement envers l'innovation, la durabilité et l'excellence dans
            la
            fabrication se reflète dans chacun de nos produits. Nous nous engageons également à réduire notre empreinte
            environnementale en adoptant des pratiques respectueuses de l'environnement tout au long de notre chaîne
            d'approvisionnement.</p>
        </div>
      </div>
      <div class="mx-auto mt-16 flex max-w-2xl flex-col gap-8 lg:mx-0 lg:mt-20 lg:max-w-none lg:flex-row lg:items-end">
        <div
            class="flex flex-col-reverse justify-between gap-x-16 gap-y-8 rounded-2xl bg-gray-50 p-8 sm:w-3/4 sm:max-w-md sm:flex-row-reverse sm:items-end lg:w-72 lg:max-w-none lg:flex-none lg:flex-col lg:items-start">
          <p class="flex-none text-3xl font-bold tracking-tight text-gray-900">250k</p>
          <div class="sm:w-80 sm:shrink lg:w-auto lg:flex-none">
            <p class="text-lg font-semibold tracking-tight text-gray-900">Users on the platform</p>
            <p class="mt-2 text-base leading-7 text-gray-600">Vel labore deleniti veniam consequuntur sunt nobis.</p>
          </div>
        </div>
        <div
            class="flex flex-col-reverse justify-between gap-x-16 gap-y-8 rounded-2xl bg-gray-900 p-8 sm:flex-row-reverse sm:items-end lg:w-full lg:max-w-sm lg:flex-auto lg:flex-col lg:items-start lg:gap-y-44">
          <p class="flex-none text-3xl font-bold tracking-tight text-white">$8.9 billion</p>
          <div class="sm:w-80 sm:shrink lg:w-auto lg:flex-none">
            <p class="text-lg font-semibold tracking-tight text-white">We’re proud that our customers have made over $8
              billion in total revenue.</p>
            <p class="mt-2 text-base leading-7 text-gray-400">Eu duis porta aliquam ornare. Elementum eget magna
              egestas.</p>
          </div>
        </div>
        <div
            class="flex flex-col-reverse justify-between gap-x-16 gap-y-8 rounded-2xl bg-indigo-600 p-8 sm:w-11/12 sm:max-w-xl sm:flex-row-reverse sm:items-end lg:w-full lg:max-w-none lg:flex-auto lg:flex-col lg:items-start lg:gap-y-28">
          <p class="flex-none text-3xl font-bold tracking-tight text-white">401,093</p>
          <div class="sm:w-80 sm:shrink lg:w-auto lg:flex-none">
            <p class="text-lg font-semibold tracking-tight text-white">Transactions this year</p>
            <p class="mt-2 text-base leading-7 text-indigo-200">Eu duis porta aliquam ornare. Elementum eget magna
              egestas. Eu duis porta aliquam ornare.</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Content section -->
    <div class="mx-auto mt-32 max-w-7xl px-6 sm:mt-40 lg:px-8">
      <div class="mx-auto flex max-w-2xl flex-col items-end justify-between gap-16 lg:mx-0 lg:max-w-none lg:flex-row">
        <div class="w-full lg:max-w-lg lg:flex-auto">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Rencontrez Notre Équipe</h2>
          <p class="mt-6 text-xl leading-8 text-gray-600">Derrière chaque produit DZ Ceram Sanitary se trouve une équipe
            dévouée de professionnels passionnés par leur métier. Nous sommes fiers de travailler avec des experts de
            l'industrie qui partagent notre vision d'excellence. Lorsque vous choisissez DZ Ceram, vous choisissez une
            équipe qui se soucie véritablement de votre satisfaction.</p>
          <img
              src="https://images.unsplash.com/photo-1547895749-888a559fc2a7?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1964&q=8004&q=80"
              alt=""
              class="mt-16 aspect-[6/5] w-full rounded-2xl bg-gray-50 object-cover lg:aspect-auto lg:h-[34.5rem]"/>
        </div>
        <div class="w-full">
          <div class="grid grid-cols-1">
            <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:col-span-2 lg:gap-8">
              <div class="rounded-2xl bg-gray-50 p-10">
                <h3 class="text-base font-semibold leading-7 text-gray-900">Los Angeles</h3>
                <address class="mt-3 space-y-1 text-sm not-italic leading-6 text-gray-600">
                  <p>4556 Brendan Ferry</p>
                  <p>Los Angeles, CA 90210</p>
                </address>
              </div>
              <div class="rounded-2xl bg-gray-50 p-10">
                <h3 class="text-base font-semibold leading-7 text-gray-900">New York</h3>
                <address class="mt-3 space-y-1 text-sm not-italic leading-6 text-gray-600">
                  <p>886 Walter Street</p>
                  <p>New York, NY 12345</p>
                </address>
              </div>
              <div class="rounded-2xl bg-gray-50 p-10">
                <h3 class="text-base font-semibold leading-7 text-gray-900">Toronto</h3>
                <address class="mt-3 space-y-1 text-sm not-italic leading-6 text-gray-600">
                  <p>7363 Cynthia Pass</p>
                  <p>Toronto, ON N3Y 4H8</p>
                </address>
              </div>
              <div class="rounded-2xl bg-gray-50 p-10">
                <h3 class="text-base font-semibold leading-7 text-gray-900">Chicago</h3>
                <address class="mt-3 space-y-1 text-sm not-italic leading-6 text-gray-600">
                  <p>726 Mavis Island</p>
                  <p>Chicago, IL 60601</p>
                </address>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </Layout>
</template>
