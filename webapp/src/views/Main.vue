<template>
  <div>
    <h1>En gros c'est mon portfolio</h1>
    <img :src="image_moi" alt="" />
    <p>À terme promis je mettrai plus de CSS</p>
    <KPIBadgeSection />
  </div>
</template>

<script setup lang="ts">
import image_moi from "@/assets/moi.jpg";
import KPIBadgeSection from "@/components/KPIBadgeSection.vue";
</script>

<style>
h1 {
  font-size: large;
  font-weight: bold;
}
</style>
