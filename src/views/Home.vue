<script setup>
import Section from "@/components/Section.vue";
import ParagraftRed from "@/components/Paragraft/ParagraftRed.vue";
import Title from "@/components/Paragraft/Title.vue";
import Button from "@/components/Button.vue";
import WebDevImg from "@/assets/img/web-dev-card.png";
import DesignImg from "@/assets/img/design-card.png";
import ContentWritingCard from "@/assets/img/content-writing-card.png";
import CardService from "@/components/Card/CardService.vue";
</script>

<template>
  <Section>
    <div class="flex items-start gap-14 mt-[150px] justify-between">
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
        class="flex-1 max-w-[450px] h-[450px] rounded-full bg-secondary mx-auto"
      ></div>
    </div>
  </Section>
  <!-- Service -->
  <Section>
    <div class="flex flex-col my-[150px]">
      <div class="flex flex-col gap-4 justify-center items-center">
        <ParagraftRed> our service </ParagraftRed>
        <Title
          >We provide great services for our customers based on needs</Title
        >
      </div>

      <div class="flex justify-center flex-wrap mt-10 gap-5">
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
    </div>
  </Section>
</template>
