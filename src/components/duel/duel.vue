<script setup>
import WaitingGame from "./waitingGame/waitingGame.vue";
import SelectThemes from "./waitingGame/selectThemes/selectThemes.vue";
import Round from "./game/round.vue";
import CorrectAnswer from "./game/correctAnswer.vue";
import WrongAnswer from "./game/wrongAnswer.vue";
import YouWin from "./game/gameFinish/youWin.vue";
import YouLose from "./game/gameFinish/youLose.vue";
import { inject } from "vue";
const { EnemySyOn, EnemySy } = inject("test");
const { ViborOn } = inject("testTwo");
</script>

<template>
  <WaitingGame v-if="!EnemySy" />
  <!-- <SelectThemes /> -->
  <!-- <Round v-if="EnemySy && !ViborOn" /> -->
  <!-- <CorrectAnswer v-if="ViborOn" /> -->
  <!-- <WrongAnswer /> -->
  <!-- <YouWin /> -->
  <!-- <YouLose /> -->
</template>

<style scoped></style>
