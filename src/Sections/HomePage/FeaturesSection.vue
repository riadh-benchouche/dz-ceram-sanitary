<script setup>
import {
  HomeIcon,
  ShieldCheckIcon,
  SparklesIcon,
  UserGroupIcon
} from '@heroicons/vue/24/outline'

const features = [
  {
    name: 'Gamme Variée de Produits Sanitaires',
    description:
        'Explorez notre large éventail de produits sanitaires allant des toilettes élégantes aux cuvettes performantes, conçus pour répondre à vos besoins spécifiques.',
    icon: SparklesIcon,
  },
  {
    name: 'Design Élégant et Fonctionnalité',
    description:
        'Fusionnant le design raffiné avec une fonctionnalité de pointe, nos produits apportent une touche d\'élégance à votre espace tout en optimisant son utilisation.',
    icon: HomeIcon,
  },
  {
    name: 'Qualité Supérieure et Durabilité',
    description:
        'Notre engagement envers la qualité inégalée et la durabilité assure des produits sanitaires qui résistent à l\'épreuve du temps et aux rigueurs de l\'utilisation quotidienne.',
    icon: ShieldCheckIcon,
  },
  {
    name: 'Expertise Locale et Service Clientèle',
    description:
        'Bénéficiez de notre expertise locale dans le domaine des produits sanitaires, soutenue par un service clientèle dévoué qui vous guide à chaque étape de votre choix.',
    icon: UserGroupIcon,
  },
]
</script>
<template>
  <div class="py-16 sm:py-20">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <p class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Notre Offre de Produits
          Sanitaires</p>
        <p class="mt-6 text-lg leading-8 text-gray-600">Découvrez comment notre engagement envers l'excellence, le
          design et la durabilité se traduit dans notre gamme complète de produits sanitaires. Explorez des options
          conçues pour rehausser votre espace tout en offrant une fonctionnalité exceptionnelle.</p>
      </div>
      <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
        <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16">
          <div v-for="(feature, index) in features" :key="index" class="relative pl-16">
            <dt class="text-base font-semibold leading-7 text-gray-900">
              <div class="absolute left-0 top-1.5 flex h-10 w-10 items-center justify-center rounded-lg bg-primary">
                <component :is="feature.icon" class="h-6 w-6 text-white" aria-hidden="true"/>
              </div>
              {{ feature.name }}
            </dt>
            <dd class="mt-1 text-base leading-6 text-gray-600">{{ feature.description }}</dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>
