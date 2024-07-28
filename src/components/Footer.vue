<script setup>
import { ref } from "vue";
import Button from "./Button.vue";
import Title from "./Paragraft/Title.vue";
import Section from "./Section.vue";

const IconLink = ref([
  {
    icon: "fa-twitter",
    url: "/",
  },
  {
    icon: "fa-facebook",
    url: "/",
  },
  {
    icon: "fa-instagram",
    url: "/",
  },
  {
    icon: "fa-linkedin",
    url: "/",
  },
]);

const LinkFooter = ref([
  {
    name: "Company",
    titleUrl: ["About us", "Contact us", "Careers", "Forums"],
  },
  {
    name: "Product",
    titleUrl: ["Features", "Pricing", "News", "Help desk", "Support"],
  },
  {
    name: "Services",
    titleUrl: [
      "Digital Marketing",
      "Content Writting",
      "Seo for Buiness",
      "UI Design",
    ],
  },
  {
    name: "Legal",
    titleUrl: ["Privacy Policy", "Terms"],
  },
]);
</script>

<template>
  <Section class="bg-primary text-white py-20">
    <div class="flex justify-between items-center">
      <div class="flex flex-col gap-y-4">
        <Title class="text-start">Ready to launch your next project</Title>
        <p class="opacity-80">
          With lots of unique blocks, you can easily build a page withour
          coding.
        </p>
      </div>
      <Button>Get started a project</Button>
    </div>

    <div class="pt-20 flex gap-10 justify-between">
      <div class="flex flex-col gap-y-5 max-w-[300px]">
        <Title class="text-start">Xendara.io</Title>
        <p class="opacity-80">
          With lots of unique blocks, you can easily build a page withour
          coding.
        </p>

        <div class="flex gap-4">
          <div v-for="(item, index) in IconLink" :key="index">
            <v-icon
              :name="item.icon"
              class="hover:fill-emerald-400"
              scale="1.5"
            />
          </div>
        </div>
      </div>
      <div class="w-full flex justify-between max-w-[800px]">
        <div
          class="flex flex-col gap-y-3"
          v-for="(item, index) in LinkFooter"
          :key="index"
        >
          <span class="opacity-70 pointer-events-none">{{ item.name }}</span>
          <span
            v-for="(link, i) in item.titleUrl"
            :key="i"
            class="pointer-events-none"
          >
            {{ link }}
          </span>
        </div>
      </div>
    </div>
  </Section>
</template>
