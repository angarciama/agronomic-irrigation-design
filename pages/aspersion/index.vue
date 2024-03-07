<template>
  <div>
    <h1>Aspersión</h1>
    <div class="form-container">
      <fieldset>
        <label for="wcc">Wcc (%) - Humedad a capacidad de campo:</label>
        <input id="wcc" v-model="wcc" type="number" min="0" max="100" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="wpmp">Wpmp (%) - Humedad a punto de marchitez permanente:</label>
        <input id="wpmp" v-model="wpmp" type="number" min="0" max="100" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="da">Da (gr/cc) - Densidad aparente:</label>
        <input id="da" v-model="da" type="number" min="0" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="pe">Pe (mm) - Profundidad efectiva de raíces:</label>
        <input id="pe" v-model="pe" type="number" min="0" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="f">F (%) - Factor de agotamiento:</label>
        <input id="f" v-model="f" type="number" min="0" max="100" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="etc">ETc (mm/día) - Evapotranspiración potencial:</label>
        <input id="etc" v-model="etc" type="number" min="0" step="0.01" required>
      </fieldset>

      <fieldset>
        <label for="eff">Eff (%) - Eficiencia de aplicación:</label>
        <input id="eff" v-model="eff" type="number" min="0" max="100" step="0.01" required>
      </fieldset>
    </div>
    <ButtonNavigate route="back" buttonText="Volver" />
  </div>
</template>

<script setup lang="ts">
import ButtonNavigate from "~/components/buttons/ButtonNavigate.vue";
import { ref } from 'vue'

const wcc = ref(null)
const wpmp = ref(null)
const da = ref(null)
const pe = ref(null)
const f = ref(null)
const etc = ref(null)
const eff = ref(null)
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