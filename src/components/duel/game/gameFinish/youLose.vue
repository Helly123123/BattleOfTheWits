<script setup>
import Header from "./gameFinishHeader.vue";
import ResultGame from "./resultFight.vue";
</script>

<template>
  <Header />
  <section class="lose-cont">
    <h2 class="lose-title">You lose</h2>
    <ResultGame />
  </section>
  <div class="button-color-cont"></div>
  <div class="button-cont">
    <h1 class="elo-lose-title">-15 <span class="elo-title">elo</span></h1>
    <button class="home-button">HOME</button>
  </div>
</template>

<style scoped>
.lose-cont {
  position: fixed;
  top: 350px;
  left: 50%;
  transform: translate(-50%, -50%);
}

.lose-title {
  margin-top: 100px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 32px;
  color: #ff6666;
  text-transform: uppercase;
  text-align: center;
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

.elo-lose-title {
  border-radius: 80px;
  width: 388px;
  height: 42px;
  background: #0053ad;
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
</style>
