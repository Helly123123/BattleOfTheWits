<script>

</script>

<template>
<section>
    <img class="light-img" src="/main/duel/enemyFound/light.svg" alt="">
    <article class="enemy-block">
        <img class="enemy-img" src="/main/duel/enemyFound/enemy_icom.svg" alt="">
        <img  src="/main/duel/enemyFound/enemy.svg" alt="">
        <div class="enemy-info">
            <h1 class="name-enemy">@username</h1>
            <h2 class="elo-enemy">1750 <span class="elo-title">elo</span></h2>
        </div>
    </article>
    <img class="fight-icon" src="/main/duel/enemyFound/fight.svg" alt="">
    <article class="user-block">
        <img class="user-img" src="/main/duel/enemyFound/user_icon.svg" alt="">
        <img  src="/main/duel/enemyFound/user.svg" alt="">
        <div class="user-info">
            <h1 class="name-user">@username</h1>
            <h2 class="elo-user">1750 <span class="elo-title">elo</span></h2>
        </div>
    </article>
</section>
</template>

<style scoped>
.enemy-block {
    position: fixed;
    top: 150px;
    left: 50%;
    transform: translate(-50%,-50%);
}

.fight-icon {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}

.light-img {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}

.user-block {
    position: fixed;
    top: 770px;
    left: 50%;
    transform: translate(-50%,-50%);
}

.enemy-img {
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translate(-50%,-50%);
}

.user-img {
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translate(-50%,-50%);
}

.enemy-info {
    position: absolute;
    top: 105px;
    left: 50%;
    transform: translate(-50%,-50%);
}

.user-info {
    position: absolute;
    top: 105px;
    left: 50%;
    transform: translate(-50%,-50%);
}

.name-enemy {
    font-family: "Inter Tight", sans-serif;
    font-weight: 400;
font-size: 20px;
text-align: center;
color: #8e460b;
margin-bottom: -30px;
}

.elo-enemy {
    font-family: "Inter Tight", sans-serif;
    font-weight: 600;
font-size: 40px;
text-align: center;
color: #8e460b;
display: flex;
align-items: center;
}

.name-user {
    font-family: "Inter Tight", sans-serif;
    font-weight: 400;
font-size: 20px;
text-align: center;
color: #5900b2;
margin-bottom: -30px;
}

.elo-user {
    font-family: "Inter Tight", sans-serif;
    font-weight: 600;
font-size: 40px;
text-align: center;
color: #5900b2;
display: flex;
align-items: center;
}

.elo-title {
font-size: 25px;
margin-top: -15px;
}

</style>