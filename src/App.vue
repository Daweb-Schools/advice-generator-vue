
<template>
  <main>
    <AdviceGenerator />
  </main>
</template>

<script>
import AdviceGenerator from "./components/AdviceGenerator.vue";

export default {
  data() {
    return {};
  },
  components: {
    AdviceGenerator,
  },
};
</script>

<style>
@import "./assets/base.css";

#app {
  max-width: 1280px;
  margin: 0 auto;
  padding: 2rem;
  font-weight: normal;
}

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

@media (min-width: 1024px) {
  body {
    display: flex;
    place-items: center;
  }
}
</style>
