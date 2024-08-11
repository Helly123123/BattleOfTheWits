<script setup>
import Header from "./headerInfo.vue";
import Question from "./question.vue";
import answerVariations from "./answerVariations.vue";
</script>

<template>
  <Header />
  <Question />
  <div class="answer-variations-cont"></div>
  <answerVariations />
</template>

<style scoped>
.answer-variations-cont {
  border-radius: 28px 28px 0 0;
  width: 100%;
  height: 516px;
  position: fixed;
  bottom: 0;
  z-index: 20;
  opacity: 60%;
  background-color: #040720;
}
</style>
