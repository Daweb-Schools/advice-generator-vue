<script setup>
import IconDice from "./design/IconDice.vue";
import DividerPattern from "./design/DividerPattern.vue";
import { ref, onMounted } from "vue";
const advice = ref({});

async function rollDice() {
  await fetch("https://api.adviceslip.com/advice")
    .then((response) => response.json())
    .then((data) => {
      advice.value = data.slip;
    });
}

rollDice();
</script>


<template>
  <div class="advice-generator">
    <div class="advice-content">
      <h1 class="advice-title">Advice #{{ advice.id }}</h1>
      <p class="advice-text">“{{ advice.advice }}”</p>

      <DividerPattern />
    </div>
    <IconDice @click="rollDice" />
  </div>
</template>



<style scoped>
.advice-generator {
  position: relative;
  width: 700px;
}

.advice-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  background-color: #313a49;
  border-radius: 0.5rem;
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.1);
}

.advice-title {
  color: #52ffa8;
  font-size: 14px;
  letter-spacing: 4px;
  text-transform: uppercase;
  margin-bottom: 15px;
}

.advice-text {
  color: #cee3e9;
  font-size: 28px;
}

.divider-pattern {
  margin: 2rem auto;
}

.dice-icon {
  position: absolute;
  bottom: -30px;
  left: 50%;
  transform: translateX(-50%);
}
</style>
