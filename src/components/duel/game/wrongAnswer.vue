<script setup>
import Header from "./headerInfo.vue";
import Question from "./question.vue";
</script>

<template>
  <Header />
  <Question />
  <section>
    <section class="answer-variations">
      <section class="answer-variations-card-cont">
        <article class="answer-variations-card-lose">
          <h1 class="answer-title">42</h1>
        </article>
        <article class="answer-variations-card-good">
          <h1 class="answer-title">42</h1>
        </article>
        <article class="answer-variations-card">
          <h1 class="answer-title">42</h1>
          <img
            class="enemy-img"
            src="/main/duel/correctAnswer/enemy.svg"
            alt="enemy"
          />
        </article>
        <article class="answer-variations-card">
          <h1 class="answer-title">42</h1>
        </article>
      </section>
      <button class="next-button">
        NEXT <img src="/main/duel/correctAnswer/NEXT.svg" alt="next" />
      </button>
    </section>
  </section>
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

.answer-variations-card-lose {
  border: 1px solid #040720;
  border-radius: 27px;
  width: 190px;
  height: 110px;
  box-shadow: 0 4px 0 0 #040720;
  box-shadow: 0 4px 0 0 #040720;
  background: linear-gradient(180deg, #f66 0%, #f33 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  opacity: 100%;
}

.answer-variations-card {
  border: 1px solid #040720;
  border-radius: 27px;
  width: 190px;
  height: 110px;
  box-shadow: 0 4px 0 0 #040720;
  box-shadow: 0 4px 0 0 #040720;
  background: linear-gradient(180deg, #2c3580 0%, #153659 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  opacity: 100%;
}

.answer-variations-card-good {
  border: 1px solid #040720;
  border-radius: 27px;
  width: 190px;
  height: 110px;
  box-shadow: 0 4px 0 0 #040720;
  background: linear-gradient(180deg, #3ccdbe 0%, #1a655e 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  opacity: 100%;
}

.answer-variations-card-color {
  border: 1px solid #040720;
  border-radius: 27px;
  width: 190px;
  height: 110px;
  opacity: 60%;
  background-color: #040720;
}

.answer-variations {
  border-radius: 28px 28px 0 0;
  width: 428px;
  height: 516px;
  position: fixed;
  bottom: 0;
  z-index: 30;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

.answer-variations-card-cont {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
  margin-top: 30px;
  position: fixed;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.answer-title {
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 18px;
  color: white;
}

.enemy-img {
  position: absolute;
  top: 70px;
  left: 15px;
}

.next-button {
  border-radius: 80px;
  width: 388px;
  height: 65px;
  background: linear-gradient(180deg, #b266ff 0%, #5900b2 100%);
  border: none;
  margin-top: 150px;
  position: fixed;
  top: 75%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: "Inter Tight", sans-serif;
  font-weight: 600;
  font-size: 22px;
  color: white;
  gap: 240px;
}
</style>
