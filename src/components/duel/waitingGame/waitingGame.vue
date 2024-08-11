<script setup>
import UserIcon from "./userIconWaiting.vue";
import EnemyFound from "./enemyFound.vue";
</script>

<template>
  <section>
    <!-- <article class="game-timer-cont">
      <p class="subtitle-timer">waiting game...</p>
      <h2 class="timer">15</h2>
    </article>
    <UserIcon />
    <article>
        <button class="cansel-button">CANCEL</button>
      </article> -->
      <!-- <EnemyFound/> -->
  </section>
</template>

<style scoped>
.game-timer-cont {
  position: fixed;
  top: 100px;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}

.subtitle-timer {
  font-family: "Inter Tight", sans-serif;
  font-weight: 400;
  font-size: 18px;
  color: rgb(255, 255, 255);
  margin-bottom: -30px;
}

.timer {
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 48px;
  color: #3ccdbe;
}

.cansel-button {
  position: fixed;
  top: 780px;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 80px;
  padding: 17px 28px;
  width: 388px;
  height: 65px;
  background: linear-gradient(180deg, #f66 0%, #f33 100%);
  border: none;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 22px;
  color: white;
}
</style>
