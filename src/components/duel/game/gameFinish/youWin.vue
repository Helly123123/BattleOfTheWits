<script setup>
import Header from "./gameFinishHeader.vue";
import ResultGame from "./resultFight.vue";
import { ref } from "vue";
const round = ref(false);
const roundOn = () => {
  round.value = true;
  console.log("sds");
};
import YouLose from "./youLose.vue";
</script>

<template>
  <YouLose v-if="round" />
  <section v-if="!round">
    <button @click="roundOn" class="nexts">Далее</button>
    <Header />
    <section class="win-cont">
      <h2 class="win-title">You Win</h2>
      <ResultGame />
    </section>
    <div class="button-color-cont"></div>
    <div class="button-cont">
      <h1 class="elo-win-title">+15 <span class="elo-title">elo</span></h1>
      <button class="home-button">HOME</button>
    </div>
  </section>
</template>

<style scoped>
.theme-win {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 30px;
  margin-top: 20px;
}

.win-title {
  margin-top: 100px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 32px;
  text-transform: uppercase;
  text-align: center;
  color: #3ccdbe;
}

.color-cont {
  display: flex;
  align-items: center;
  gap: 12px;
}

.nexts {
  position: fixed;
  top: 70%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 60px;
  color: rgb(223, 167, 167);
  border: none;
  color: black;
  border-radius: 5px;
  z-index: 100;
}

.win-cont {
  position: fixed;
  top: 350px;
  left: 50%;
  transform: translate(-50%, -50%);
}

.button-color-cont {
  border-radius: 28px 28px 0 0;
  width: 100%;
  height: 193px;
  position: fixed;
  bottom: 0;
  z-index: 20;
  opacity: 60%;
  background-color: #040720;
}

.button-cont {
  position: fixed;
  bottom: 0;
  z-index: 30;
  width: 100%;
  height: 193px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.elo-win-title {
  border-radius: 80px;
  width: 388px;
  height: 42px;
  background: #3395ff;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 28px;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}

.elo-title {
  font-size: 18px;
  margin-top: -10px;
}

.home-button {
  border-radius: 80px;
  width: 388px;
  height: 65px;
  background: linear-gradient(180deg, #b266ff 0%, #5900b2 100%);
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 22px;
  color: white;
  border: none;
}
@media screen and (max-width: 390px) {
  .home-button {
    width: 360px;
    height: 65px;
    font-size: 22px;
  }

  .elo-win-title {
    width: 360px;
    height: 42px;
    font-size: 28px;
  }
}

@media screen and (max-width: 360px) {
  .home-button {
    width: 340px;
    height: 55px;
    font-size: 22px;
  }

  .elo-win-title {
    width: 340px;
    height: 42px;
    font-size: 28px;
  }
}

@media screen and (max-width: 340px) {
  .home-button {
    width: 320px;
    height: 55px;
    font-size: 22px;
  }

  .elo-win-title {
    width: 320px;
    height: 42px;
    font-size: 28px;
  }
}
</style>
