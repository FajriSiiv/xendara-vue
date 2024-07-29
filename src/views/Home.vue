<script setup>
import Section from "@/components/Section.vue";
import ParagraftRed from "@/components/Paragraft/ParagraftRed.vue";
import Title from "@/components/Paragraft/Title.vue";
import Button from "@/components/Button.vue";
import Footer from "@/components/Footer.vue";

import WebDevImg from "@/assets/img/web-dev-card.png";
import DesignImg from "@/assets/img/design-card.png";
import ContentWritingCard from "@/assets/img/content-writing-card.png";
import CardService from "@/components/Card/CardService.vue";

import People1 from "@/assets/img/people-1.jpg";
import People2 from "@/assets/img/people-2.jpg";
import People3 from "@/assets/img/people-3.jpg";

import Brand1 from "@/assets/img/brand-1.jpg";
import Brand2 from "@/assets/img/brand-2.jpg";
import Brand3 from "@/assets/img/brand-3.jpg";
import Brand4 from "@/assets/img/brand-4.jpg";

import BackgroundLine from "@/assets/background/background-line.svg";

import { ref } from "vue";

const CardChoose = ref([
  {
    title: "Dedicated project manager",
    icon: "la-user-graduate-solid",
    bgColor: "bg-purple-100",
    fill: "#473BF0",
  },
  {
    title: "Organized tasks",
    icon: "la-servicestack",
    bgColor: "bg-rose-100",
    fill: "#F64B4B",
  },
  {
    title: "Easy feedback sharing",
    icon: "la-rocketchat",
    bgColor: "bg-emerald-100",
    fill: "#68D585",
  },
  {
    title: "Never miss headline",
    icon: "la-newspaper",
    bgColor: "bg-neutral-200",
    fill: "#161C2D",
  },
]);
</script>

<template>
  <Section>
    <div class="flex items-start gap-14 mt-[150px] justify-between md:mt-20">
      <div class="flex-1 flex-col flex gap-y-3 max-w-[560px]">
        <ParagraftRed>let's shift your business</ParagraftRed>

        <h1 class="text-5xl font-bold leading-tight">
          Shift your business fast with Xendara.
        </h1>

        <p class="">
          Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eius
          delectus sed autem veritatis! Iure ipsa, consequuntur laborum possimus
          fuga optio! Est, possimus doloribus. Officiis
        </p>

        <Button>Get started a project</Button>
      </div>
      <div
        class="flex-1 max-w-[450px] h-[450px] rounded-full overflow-hidden mx-auto md:hidden"
      >
        <img v-bind:src="People1" alt="people hero" />
      </div>
    </div>
  </Section>
  <!-- Service -->
  <Section>
    <div class="flex flex-col my-[150px] sm:my-14">
      <div class="flex flex-col gap-4 justify-center items-center">
        <ParagraftRed> our service </ParagraftRed>
        <Title
          >We provide great services for our customers based on needs</Title
        >
      </div>

      <div class="flex justify-center flex-wrap my-10 gap-5">
        <CardService
          :img-url="DesignImg"
          description="Bangun design web responsif dan ramah seluler untuk pengalaman konsisten di semua perangkat."
          nameService="Graphic Design"
          background="bg-primary"
        />
        <CardService
          :img-url="WebDevImg"
          description="Bangun situs web responsif dan ramah seluler untuk pengalaman konsisten di semua perangkat."
          nameService="Web Development"
        />
        <CardService
          :img-url="ContentWritingCard"
          description="Bangun situs web responsif dan ramah seluler untuk pengalaman konsisten di semua perangkat."
          nameService="Content Writting"
          background="bg-[#F64B4B]"
        />
      </div>

      <div class="flex gap-16 my-20 md:flex-col">
        <div class="max-w-[300px] max-h-[300px] w-full h-full md:mx-auto">
          <div class="h-[300px] w-[300px] overflow-hidden rounded-full">
            <img v-bind:src="People3" alt="people testimonial" />
          </div>
        </div>

        <div class="flex flex-col gap-y-5">
          <div class="flex flex-row gap-x-3">
            <div v-for="(star, index) in [1, 2, 3, 4, 5]" :key="index">
              <v-icon name="fa-star" scale="1.5" fill="#FCAD38" />
            </div>
          </div>

          <span class="font-bold text-2xl">
            &quot;Desain modern, responsif, dan intuitif. Navigasi mudah, warna
            dan tipografi konsisten. Sangat user-friendly.&quot;
          </span>

          <div class="flex flex-row gap-x-10 text-lg justify-end mt-10">
            <span class="font-bold">Henry F. </span>
            <span class="">HR PT.Indonesia Sejahtera</span>
          </div>
        </div>
      </div>
    </div>
  </Section>
  <!-- Our Story -->
  <Section>
    <div class="my-10">
      <ParagraftRed>Our Story</ParagraftRed>
      <Title class="text-start mt-5"
        >We know how everything works and why your business is failing over and
        over again.</Title
      >

      <div class="flex gap-20 my-10 lg:gap-8 md:gap-5 sm:my-3">
        <div class="flex-1 mt-10 sm:hidden">
          <div class="max-w-[500px] max-h-[500px]">
            <div class="w-full h-[500px] rounded-md relative overflow-hidden">
              <img
                v-bind:src="People1"
                class="w-full h-full object-cover"
                alt="people-1"
              />
            </div>
          </div>
        </div>
        <div class="flex-[2] -mt-7 md:flex-1">
          <div class="flex flex-col gap-y-20 md:gap-y-5">
            <div class="flex w-full relative">
              <div
                class="w-[330px] h-[330px] rounded-md relative overflow-hidden md:w-full"
              >
                <img
                  v-bind:src="People3"
                  class="w-full h-full object-cover object-top"
                  alt="people-2"
                />
              </div>
              <div
                class="w-[200px] h-[200px] rounded-md absolute right-20 -bottom-10 overflow-hidden md:hidden"
              >
                <div class="w-full h-full relative">
                  <img
                    v-bind:src="People2"
                    class="w-full h-full object-cover"
                    alt="people-2"
                  />
                </div>
              </div>
            </div>
            <p class="max-w-[600px]">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit.
              Cupiditate aliquid consequatur ex ducimus quam consectetur cumque
              eaque sed facere voluptates nostrum quod at enim eius omnis neque
              magni quo veritatis eum laboriosam suscipit, esse molestias!
              Asperiores aspernatur earum dolore doloremque laboriosam.
            </p>
          </div>
        </div>
      </div>

      <div class="flex justify-around my-32 lg:gap-10 sm:flex-col sm:my-8">
        <div
          class="flex flex-col gap-3 justify-center items-center max-w-[350px]"
        >
          <Title class="text-5xl">1M+</Title>
          <span class="text-center"
            >Customers visit Xendara every month to get their service
            done.</span
          >
        </div>
        <div
          class="flex flex-col gap-3 justify-center items-center max-w-[350px]"
        >
          <Title class="text-5xl">92%</Title>
          <span class="text-center"
            >Stafisfaction rate comes from our awesome customer.</span
          >
        </div>
        <div
          class="flex flex-col gap-3 justify-center items-center max-w-[350px]"
        >
          <Title class="text-5xl">4.9/5.0</Title>
          <span class="text-center"
            >Avarage customer ratings we have got all over internet.</span
          >
        </div>
      </div>
    </div>
  </Section>
  <!-- Why choose us -->
  <Section class="bg-slate-50 bg-opacity-70">
    <div class="py-20">
      <div class="text-center flex flex-col items-center gap-4">
        <ParagraftRed>why choose us</ParagraftRed>
        <Title>People choose us because we serve the best for everyone</Title>
      </div>

      <div
        class="mt-20 grid grid-cols-2 grid-rows-2 max-w-[900px] mx-auto gap-20 md:flex md:flex-col"
      >
        <div
          class="flex gap-x-4 items-start"
          v-for="(item, index) in CardChoose"
          :key="index"
        >
          <div
            :class="[
              'rounded-md w-20 h-20  flex items-center justify-center',
              item.bgColor,
            ]"
          >
            <v-icon :name="item.icon" scale="2" :fill="item.fill" />
          </div>
          <div class="flex flex-col gap-y-2 flex-[2]">
            <span class="font-bold text-xl">{{ item.title }}</span>
            <p class="text-sm">
              With lots of unique blocks, you can easily build a page without
              coding.Build your next landing page.
            </p>
          </div>
        </div>
      </div>

      <div
        class="flex justify-between w-full mt-40 items-center lg:gap-20 md:flex-col md:mt-20"
      >
        <div class="flex flex-col gap-y-4 max-w-[700px]">
          <h3 class="text-3xl font-bold">Ready to launch your next project?</h3>
          <p class="opacity-80">
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Reprehenderit quidem repellat accusantium deleniti libero earum.
          </p>
        </div>
        <Button class="text-nowrap">Get started a project</Button>
      </div>
    </div>
  </Section>
  <!-- Case Studies -->
  <Section>
    <div class="my-20">
      <div class="text-center flex flex-col justify-center items-center gap-4">
        <ParagraftRed>case studies</ParagraftRed>
        <Title>Our works describe why we are the best in the business</Title>
      </div>
      <div
        class="grid grid-cols-2 grid-rows-7 gap-x-10 gap-y-3 my-10 max-w-[1020px] mx-auto sm:grid-cols-1 sm:grid-rows-4"
      >
        <div class="row-span-4 h-[600px] overflow-hidden gap-y-4 flex flex-col">
          <div class="h-[454px] w-full rounded-md overflow-hidden">
            <img v-bind:src="Brand1" alt="brand1" class="object-cover h-full" />
          </div>
          <div class="flex flex-col gap-1 ml-6 mt-3">
            <span class="opacity-90">Graphic Design</span>
            <span class="font-bold text-xl">Aura Branding Design</span>
          </div>
        </div>
        <div class="row-span-3 h-[400px] overflow-hidden gap-y-4 flex flex-col">
          <div class="h-[303px] w-full rounded-md overflow-hidden">
            <img v-bind:src="Brand2" alt="brand2" class="object-cover h-full" />
          </div>
          <div class="flex flex-col gap-1 ml-6 mt-3">
            <span class="opacity-90">Graphic Design</span>
            <span class="font-bold text-xl">AB.S Snack Packaging</span>
          </div>
        </div>
        <div class="row-span-4 h-[600px] overflow-hidden gap-y-4 flex flex-col">
          <div class="h-[454px] w-full rounded-md overflow-hidden">
            <img v-bind:src="Brand4" alt="brand4" class="object-cover h-full" />
          </div>
          <div class="flex flex-col gap-1 ml-6 mt-3">
            <span class="opacity-90">Content Writting</span>
            <span class="font-bold text-xl">Magazine Content Writting</span>
          </div>
        </div>
        <div class="row-span-3 h-[400px] overflow-hidden gap-y-4 flex flex-col">
          <div class="h-[303px] w-full rounded-md overflow-hidden">
            <img v-bind:src="Brand3" alt="brand3" class="object-cover h-full" />
          </div>
          <div class="flex flex-col gap-1 ml-6 mt-3">
            <span class="opacity-90">Website Development</span>
            <span class="font-bold text-xl">Gradient Website Development</span>
          </div>
        </div>
      </div>
      <div class="w-full flex items-center justify-center">
        <Button transparent arrow>See all works</Button>
      </div>
    </div>
  </Section>
  <!-- Testimonial -->
  <Section class="bg-secondary relative overflow-hidden py-20">
    <div
      class="text-white flex flex-col gap-5 items-center justify-center z-10 relative"
    >
      <ParagraftRed class="text-white">testimonial</ParagraftRed>
      <Title class="text-white text-2xl max-w-[600px]"
        >&quot;Simply the best. Better than all the rest. I'd recommend this
        product to beginners and advanced users.&quot;</Title
      >
      <div class="flex flex-col gap-y-3 justify-center items-center">
        <div class="w-20 h-20 rounded-full overflow-hidden">
          <img v-bind:src="People1" alt="" />
        </div>

        <span class="font-semibold">Morgana. S</span>
      </div>
    </div>
    <div class="absolute left-1/5 top-0 w-full h-full">
      <img v-bind:src="BackgroundLine" alt="background line testimonial" />
    </div>
  </Section>
  <!-- Footer -->
  <Footer></Footer>
</template>
