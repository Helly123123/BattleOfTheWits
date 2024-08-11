<script>
export default {
  data() {
    return {
      themeStatiom: {
        black: true,
        trec: true,
        fuc: true,
        chet: 0,
      },
      styletest: {
        opacity: "100px",
      },
    };
  },
  methods: {
    clock() {
      if (this.themeStatiom.chet != 2) {
        this.themeStatiom.chet++;
        this.themeStatiom.black = false;
      }
    },
    clockT() {
      if (this.themeStatiom.chet != 2) {
        this.themeStatiom.chet++;
        this.themeStatiom.fuc = false;
      }
    },
    clockH() {
      if (this.themeStatiom.chet != 2) {
        this.themeStatiom.chet++;
        this.themeStatiom.trec = false;
      }
    },
  },
};
</script>

<template>
  <section class="theme-cont">
    <h2 class="theme-title">
      Choose 2 out of 6 themes<br />
      for the questions
    </h2>
    <section class="there-card-cont">
      <article
        @click="clock"
        class="theme-card"
        :class="{
          opacity: themeStatiom.chet === 2,
        }"
      >
        <div v-if="themeStatiom.black" class="theme-card-color"></div>
        <img src="/main/selectThemes/Science.svg" alt="" />
        <h2 class="theme-card-title">Science</h2>
      </article>
      <article
        @click="clockT"
        class="theme-card"
        :class="{ opacity: themeStatiom.chet === 2 }"
      >
        <div v-if="themeStatiom.fuc" class="theme-card-color"></div>
        <img src="/main/selectThemes/In_a_healthy_body.svg" alt="" />
        <h2 class="theme-card-title">In a healthy body</h2>
      </article>
      <article
        @click="clockH"
        class="theme-card"
        :class="{ opacity: themeStatiom.chet === 2 }"
      >
        <div v-if="themeStatiom.trec" class="theme-card-color"></div>
        <img src="/main/selectThemes/In_the_world_of_cinema.svg" alt="" />
        <h2 class="theme-card-title">In the world of cinema</h2>
      </article>
      <article
        @click="clock"
        class="theme-card"
        :class="{ opacity: themeStatiom.chet === 2 }"
      >
        <div class="theme-card-color"></div>
        <img src="/main/selectThemes/Games_and_video_games.svg" alt="" />
        <h2 class="theme-card-title">Games and video games</h2>
      </article>
      <article
        @click="clock"
        class="theme-card"
        :class="{ opacity: themeStatiom.chet === 2 }"
      >
        <div class="theme-card-color"></div>
        <img src="/main/selectThemes/history.svg" alt="" />
        <h2 class="theme-card-title">History</h2>
      </article>
      <article
        @click="clock"
        class="theme-card"
        :class="{ opacity: themeStatiom.chet === 2 }"
      >
        <div class="theme-card-color"></div>
        <img src="/main/selectThemes/Music.svg" alt="" />
        <h2 class="theme-card-title">Music</h2>
      </article>
      <article
        @click="clock"
        class="theme-card"
        :class="{ opacity: themeStatiom.chet === 2 }"
      >
        <div class="theme-card-color"></div>
        <img src="/main/selectThemes/Geography.svg" alt="" />
        <h2 class="theme-card-title">Geography</h2>
      </article>
      <article
        @click="clock"
        class="theme-card"
        :class="{ opacity: themeStatiom.chet === 2 }"
      >
        <div class="theme-card-color"></div>
        <img src="/main/selectThemes/TV_series.svg" alt="" />
        <h2 class="theme-card-title">TV series</h2>
      </article>
    </section>
  </section>
</template>

<style scoped>
.theme-cont {
  position: fixed;
  top: 350px;
  left: 50%;
  transform: translate(-50%, -50%);
}

.theme-title {
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 32px;
  color: white;
}

.there-card-cont {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 10px;
}

.theme-card-title {
  position: absolute;
  top: 70px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 14px;
  text-align: center;
  color: white;
}

.theme-card img {
  position: absolute;
  top: 15px;
  width: 60px;
  height: 60px;
}

.theme-card {
  border: 1px solid #040720;
  border-radius: 27px;
  width: 190px;
  height: 117px;
  box-shadow: 0 4px 0 0 #040720;
  background: linear-gradient(180deg, #3395ff 0%, #0053ad 100%),
    rgba(4, 7, 32, 0.6);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  position: relative;
  opacity: 100%;
}

.theme-card.opacity {
  opacity: 60%;
}

.theme-card.active {
  opacity: 100%;
}

.theme-card-color {
  border: 1px solid #040720;
  border-radius: 27px;
  width: 190px;
  height: 117px;
  opacity: 60%;
  background-color: #040720;
}
</style>
