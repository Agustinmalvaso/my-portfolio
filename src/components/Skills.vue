<script setup lang="ts">
import {
  Carousel,
  CarouselContent,
  CarouselItem,
  CarouselNext,
  CarouselPrevious,
} from "@/components/ui/carousel";
import { Card, CardContent, CardTitle } from "@/components/ui/card";

const skills = [
  {
    imageName: "vuejsLogo.jpg",
    alt: "Vue.js",
    description:
      "I have been developing interactive and dynamic user interfaces, with experience in components, directives, state management and component testing.",
  },
  {
    imageName: "laravelLogo.jpg",
    description:
      "Skilled in backend development with PHP using Laravel, including routing, controllers, Eloquent ORM, and database migrations.",
    alt: "Laravel",
  },
  {
    imageName: "mongodbLogo.png",
    description:
      "Experience in handling NoSQL databases with MongoDB, focusing on document modeling, queries, and scalability.",
    alt: "MongoDB",
  },
  {
    imageName: "mysqlLogo.jpg",
    description:
      "Focused in managing and optimizing relational databases with MySQL, including schema design, complex queries, and enhancing performance.",
    alt: "MongoDB",
  },
];
</script>

<template>
  <div class="flex flex-col justify-center items-center">
    <p class="text-white font-mono font-bold text-xl">Skills</p>
    <Carousel class="relative w-full max-w-5xl">
      <CarouselContent>
        <CarouselItem
          v-for="(skill, index) in skills"
          :key="index"
          class="md:basis-1/2 lg:basis-1/3"
        >
          <div class="p-1">
            <Card class="rounded-2xl bg-blue-950">
              <CardTitle class="text-white font-mono flex justify-center p-5"
                ><img
                  :src="`/assets/images/${skill.imageName}`"
                  alt="Vue.js"
                  class="w-60 h-32 object-cover"
              /></CardTitle>
              <CardContent
                class="flex aspect-square items-start justify-center p-6"
              >
                <span class="text-xl text-white">{{ skill.description }}</span>
              </CardContent>
            </Card>
          </div>
        </CarouselItem>
      </CarouselContent>
      <CarouselPrevious class="bg-white hover:bg-slate-300" />
      <CarouselNext class="bg-white hover:bg-slate-300" />
    </Carousel>
  </div>
</template>
