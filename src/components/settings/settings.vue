<script setup>
import { inject, reactive, ref } from "vue";
import Support from './support.vue'
const { falseSettings } = inject("settingsStation");
const { supportOn, supportActive } = inject("supportActive");

const settingsButton = reactive({
  settingsActiveLan: false,
  settingsActiveNot: false,
});



const settingsButtonLanClick = () => {
  settingsButton.settingsActiveLan = !settingsButton.settingsActiveLan;
};

const settingsButtonNotClick = () => {
  settingsButton.settingsActiveNot = !settingsButton.settingsActiveNot;
};
</script>

<template>
  <section class="settings-cont" v-if="!supportActive">
    <section class="settings-button-cont-block"></section>
    <section class="settings-button-cont">
      <article @click="falseSettings" class="settings-title-cont">
        <img src="/main/settings/left.svg" alt="out" />
        <h2 class="title-settings">Settings</h2>
      </article>
      <article>
        <button @click="supportOn" class="settings-button support">
          Support <img src="/main/settings/right.svg" alt="" />
        </button>
        <button
          class="settings-button language"
          @click="settingsButtonLanClick"
        >
          Language
          <img
            v-if="!settingsButton.settingsActiveLan"
            src="/main/settings/switch_one.svg"
            alt=""
          /><img v-else src="/main/settings/switch_two.svg" alt="" />
        </button>
        <button
          class="settings-button notifications"
          @click="settingsButtonNotClick"
        >
          Notifications
          <img
            src="/main/settings/swith_on.svg"
            alt=""
            v-if="!settingsButton.settingsActiveNot"
          /><img src="/main/settings/swith_off.svg" alt="" v-else />
        </button>
      </article>
      <article>
        <button class="settings-button agreement">
          User Agreement <img src="/main/settings/right.svg" alt="" />
        </button>
        <button class="settings-button policy">
          Privacy Policy <img src="/main/settings/right.svg" alt="" />
        </button>
      </article>
    </section>
  </section>
  <section class="suport" v-if="supportActive">
    <Support/>
  </section>
</template>

<style scoped>
.settings-cont {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 24px;
}

.settings-button-cont-block {
  border-radius: 28px 28px 0 0;
  width: 100%;
  height: 750px;
  position: fixed;
  bottom: 0;
  z-index: 20;
  background-color: hsl(234, 78%, 7%);
  opacity: 60%;
}

.settings-button-cont {
  position: fixed;
  bottom: 0;
  z-index: 30;
  width: 100%;
  height: 750px;
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 24px;
}

.settings-title-cont {
  position: absolute;
  top: -80px;
  left: 20px;
  z-index: 40;
  display: flex;
  align-items: center;
  gap: 16px;
}

.title-settings {
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 32px;
  color: rgb(255, 255, 255);
}

.settings-button {
  border: 1px solid #040720;
  border-radius: 30px;
  padding: 8px 16px;
  width: 388px;
  height: 44px;
  box-shadow: 0 4px 0 0 #040720;
  background: linear-gradient(180deg, #3395ff 0%, #0053ad 100%);
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 16px;
  color: rgb(255, 255, 255);
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0px;
  margin-top: 8px;
}

.settings-button.support {
  gap: 269px;
  margin-top: 24px;
}

.settings-button.language {
  gap: 214px;
}

.settings-button.notifications {
  gap: 194px;
}

.settings-button.agreement {
  gap: 210px;
}

.settings-button.policy {
  gap: 228px;
}

@media screen and (max-width: 390px) {
  .settings-button {
  width: 360px;
  height: 44px;
  font-size: 16px;
  margin-top: 8px;
}
.settings-button.support {
  gap: 250px;
  margin-top: 24px;
}

.settings-button.language {
  gap: 200px;
}

.settings-button.notifications {
  gap: 180px;
}

.settings-button.agreement {
  gap: 185px;
}

.settings-button.policy {
  gap: 203px;
}
}

@media screen and (max-width: 360px) {
  .settings-button {
  width: 340px;
  height: 44px;
  font-size: 16px;
  margin-top: 8px;
}
.settings-button.support {
  gap: 230px;
  margin-top: 24px;
}

.settings-button.language {
  gap: 170px;
}

.settings-button.notifications {
  gap: 150px;
}

.settings-button.agreement {
  gap: 165px;
}

.settings-button.policy {
  gap: 180px;
}
}

@media screen and (max-width: 340px) {
  .settings-button {
  width: 320px;
  height: 44px;
  font-size: 16px;
  margin-top: 8px;
}
.settings-button.support {
  gap: 210px;
  margin-top: 24px;
}

.settings-button.language {
  gap: 150px;
}

.settings-button.notifications {
  gap: 130px;
}

.settings-button.agreement {
  gap: 145px;
}

.settings-button.policy {
  gap: 160px;
}
}

</style>
