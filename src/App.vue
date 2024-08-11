<script setup>
import UserHeader from "./components/header/user_header/userHeader.vue";
import HistoryGame from "./components/userGame/historyGame.vue";
import Navigation from "./components/navigation/Navigation.vue";
import Friends from "./components/friends/friends.vue";
import Settings from "./components/settings/settings.vue";
import Duel from "./components/duel/duel.vue";
import { ref, inject, provide, reactive } from "vue";

const navigationStation = ref(true);
const settingsStation = ref(false);
const supportActive = ref(false);
const duelStation = ref(false);
const EnemySy = ref(false);
const Vibor = ref(false);
const VibotTwo = ref(false);

const VibotTwoOn = () => {
  VibotTwo.value = true;
  console.log("VibotTwo");
};
const ViborOn = () => {
  Vibor.value = true;
  console.log("Vibor");
};

const EnemySyOn = () => {
  EnemySy.value = true;
  console.log("sds");
};

const duelStationOn = () => {
  duelStation.value = true;
};
const duelStationOff = () => {
  duelStation.value = false;
};

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

const supportOn = () => {
  supportActive.value = true;
};

const supportOff = () => {
  supportActive.value = false;
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

provide("supportActive", {
  supportActive,
  supportOn,
  supportOff,
});

provide("duelStation", {
  duelStation,
  duelStationOn,
  duelStationOff,
});

provide("test", {
  EnemySy,
  EnemySyOn,
});

provide("testTwo", {
  Vibor,
  ViborOn,
  VibotTwo,
  VibotTwoOn,
});
</script>

<template>
  <div class="cont">
    <img class="bg-img" src="/bg.svg" alt="" />
  </div>
  <Duel v-if="duelStation" />
  <section class="main-section" v-if="!settingsStation && !duelStation">
    <button class="next" @click="duelStationOn">Далее</button>
    <section class="user-accaunt">
      <UserHeader />
      <button @click="duelStationOn" class="new-game-btn">
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
  <Navigation v-if="!duelStation" />
</template>

<style scoped>
html,
body {
  overflow-x: hidden;
  margin: 0;
  padding: 0;
}

.test-btn-cont {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1000;
}

.next {
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
  display: flex;
  align-items: center;
  flex-direction: column;
}

.bg-img {
  position: relative;
  height: 100%;
}

.new-game-btn {
  border-radius: 80px;
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

@media screen and (max-width: 390px) {
  .new-game-btn {
    width: 360px;
    height: 60px;
    font-size: 20px;
    gap: 50px;
  }
}

@media screen and (max-height: 900px) {
  .user-interface-cont {
    background-color: #040720;
    width: 100%;
    height: 660px;
  }
}

@media screen and (max-height: 880px) {
  .user-interface-cont {
    background-color: #040720;
    width: 100%;
    height: 630px;
  }
}

@media screen and (max-height: 870px) {
  .user-interface-cont {
    background-color: #040720;
    width: 100%;
    height: 600px;
  }
}

@media screen and (max-height: 830px) {
  .user-interface-cont {
    background-color: #040720;
    width: 100%;
    height: 550px;
  }
}

@media screen and (max-height: 780px) {
  .user-interface-cont {
    background-color: #040720;
    width: 100%;
    height: 500px;
  }
}

@media screen and (max-height: 730px) {
  .user-interface-cont {
    background-color: #040720;
    width: 100%;
    height: 450px;
  }
}

@media screen and (max-height: 680px) {
  .user-interface-cont {
    background-color: #040720;
    width: 100%;
    height: 400px;
  }
}
</style>
