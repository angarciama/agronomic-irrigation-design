<template>
  <div>
    <h1>Diseño Agronomico de Riego</h1>
    <ButtonNavigate route="back" buttonText="Volver" />
    <ButtonNavigate route="aspersion" buttonText="Aspersion" />
    <ButtonNavigate route="drip-or-microspray" buttonText="Goteo o Microaspersion" />
  </div>
</template>

<script setup lang="ts">
import ButtonNavigate from "~/components/buttons/ButtonNavigate.vue";
</script>