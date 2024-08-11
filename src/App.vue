<script setup>
import UserHeader from "./components/header/user_header/userHeader.vue";
import HistoryGame from "./components/userGame/historyGame.vue";
import Navigation from "./components/navigation/Navigation.vue";
import Friends from "./components/friends/friends.vue";
import Settings from "./components/settings/settings.vue";
import { ref, inject, provide, reactive } from "vue";

const navigationStation = ref(true);
const settingsStation = ref(false);

const falseNavigation = () => {
  navigationStation.value = false;
};
const trueNavigation = () => {
  navigationStation.value = true;
};

const falseSettings = () => {
  settingsStation.value = false;
};
const trueSettings = () => {
  settingsStation.value = true;
};

provide("navigationStation", {
  navigationStation,
  trueNavigation,
  falseNavigation,
});

provide("settingsStation", {
  settingsStation,
  falseSettings,
  trueSettings,
});
</script>

<template>
  <div class="cont">
    <img class="bg-img" src="/bg.svg" alt="" />
  </div>
  <section class="main-section" v-if="!settingsStation">
    <section class="user-accaunt">
      <UserHeader />
      <button class="new-game-btn">
        <img src="/main/sword.svg" alt="" />
        NEW GAME
        <img src="/main/sword.svg" alt="" />
      </button>
    </section>
    <section class="user-interface-cont"></section>
    <HistoryGame v-if="navigationStation" />
    <Friends v-else />
  </section>
  <Settings v-if="settingsStation" />
  <Navigation />
</template>

<style scoped>
html,
body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}

.user-interface-cont {
  position: fixed;
  bottom: 0;
  z-index: 20;
  border-radius: 28px 28px 0 0;
  background-color: #040720;
  opacity: 60%;
  width: 100%;
  height: 673px;
}

.cont {
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}

.user-accaunt {
  position: absolute;
  top: 140px;
  left: 50%;
  transform: translate(-50%, -50%);
}

.bg-img {
  position: relative;
}

.new-game-btn {
  border-radius: 80px;
  padding: 17px 28px;
  width: 388px;
  height: 65px;
  background: linear-gradient(180deg, #3395ff 0%, #0053ad 100%);
  border: none;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 22px;
  text-transform: uppercase;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 70px;
}
</style>
