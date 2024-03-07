<template>
  <div>
    <h1>Goteo o Microaspesión</h1>
    <div class="form-container">
      <fieldset>
        <label for="fr">Fr (día) - Frecuencia de riego:</label>
        <input id="fr" v-model="fr" type="number" min="0" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="etc">ETc (mm/día) - Evapotranspiración potencial:</label>
        <input id="etc" v-model="etc" type="number" min="0" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="eff">Eff (%) - Eficiencia de aplicación:</label>
        <input id="eff" v-model="eff" type="number" min="0" max="100" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="ip">Ip (mm/día) - Intensidad de precipitación del emisor:</label>
        <input id="ip" v-model="ip" type="number" min="0" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="hld">Hld (h) - Horas laborales al día:</label>
        <input id="hld" v-model="hld" type="number" min="0" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="totalMod">Total mod (#) - Total de módulos a regar:</label>
        <input id="totalMod" v-model="totalMod" type="number" min="0" step="1" required>
      </fieldset>
    </div>
    <ButtonNavigate route="back" buttonText="Volver" />
  </div>
</template>

<script setup lang="ts">
import ButtonNavigate from "~/components/buttons/ButtonNavigate.vue";
import { ref } from 'vue'

const fr = ref(null)
const etc = ref(null)
const eff = ref(null)
const ip = ref(null)
const hld = ref(null)
const totalMod = ref(null)
</script>

<style scoped>
.form-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
}
fieldset {
  display: flex;
  border: none;
  margin-bottom: 10px;
}
label {
  font-weight: bold;
  margin-bottom: 5px;
}

input {
  border: 1px solid black;
  border-radius: 10px;
  height: 20px;
  background-color: white;
  color: black;
  font-weight: bold;
  cursor: pointer;
  padding: 0 20px;
}
input:hover {
  background-color: black;
  color: white;
}
input:active {
  background-color: black;
  color: white;
}
</style>