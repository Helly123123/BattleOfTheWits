<script></script>

<template>
  <section>
    <article class="theme-win">
      <div class="color-cont">
        <img src="/main/duel/round/color/green.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="red" />
        <img src="/main/duel/round/color/green.svg" alt="green" />
      </div>
      <article class="theme">
        <img src="/main/selectThemes/Science.svg" alt="" />
        <h2 class="theme-title">Science</h2>
      </article>
      <div class="color-cont">
        <img src="/main/duel/round/color/green.svg" alt="green" />
        <img src="/main/duel/round/color/green.svg" alt="green" />
        <img src="/main/duel/round/color/green.svg" alt="green" />
      </div>
    </article>
    <article class="theme-win">
      <div class="color-cont">
        <img src="/main/duel/round/color/green.svg" alt="green" />
        <img src="/main/duel/round/color/green.svg" alt="red" />
        <img src="/main/duel/round/color/green.svg" alt="green" />
      </div>
      <article class="theme">
        <img src="/main/selectThemes/Science.svg" alt="" />
        <h2 class="theme-title">
          Games and<br />
          video games
        </h2>
      </article>
      <div class="color-cont">
        <img src="/main/duel/round/color/green.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="green" />
        <img src="/main/duel/round/color/green.svg" alt="green" />
      </div>
    </article>
    <article class="theme-win">
      <div class="color-cont">
        <img src="/main/duel/round/color/green.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="red" />
        <img src="/main/duel/round/color/red.svg" alt="green" />
      </div>
      <article class="theme">
        <img src="/main/selectThemes/Science.svg" alt="" />
        <h2 class="theme-title">Science</h2>
      </article>
      <div class="color-cont">
        <img src="/main/duel/round/color/red.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="green" />
      </div>
    </article>
    <article class="theme-win">
      <div class="color-cont">
        <img src="/main/duel/round/color/green.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="red" />
        <img src="/main/duel/round/color/red.svg" alt="green" />
      </div>
      <article class="theme">
        <img src="/main/selectThemes/Science.svg" alt="" />
        <h2 class="theme-title">Science</h2>
      </article>
      <div class="color-cont">
        <img src="/main/duel/round/color/red.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="green" />
        <img src="/main/duel/round/color/red.svg" alt="green" />
      </div>
    </article>
  </section>
</template>

<style scoped>
.win-cont {
  position: fixed;
  top: 350px;
  left: 50%;
  transform: translate(-50%, -50%);
}

.theme-title {
  font-family: "Inter Tight", sans-serif;
  font-weight: 400;
  font-size: 12px;
  color: white;
}

.theme {
  border: 1px solid #040720;
  border-radius: 27px;
  width: 100px;
  height: 100px;
  box-shadow: 0 4px 0 0 #040720;
  background: linear-gradient(180deg, #2c3580 0%, #153659 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
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

.theme-win {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 30px;
  margin-top: 20px;
}

.color-cont {
  display: flex;
  align-items: center;
  gap: 12px;
}
</style>
