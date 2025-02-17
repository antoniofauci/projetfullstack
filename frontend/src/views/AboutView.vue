<template>
  <div class="about">
    <ParticipationFormulaire />

  </div>
</template>

<script setup>
import ParticipationFormulaire from "@/components/ParticipationFormulaire.vue";
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
