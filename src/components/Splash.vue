<script setup>
function playVid() {
  document.getElementById("bgVid").play();
}

function learnClick() {
  document.getElementById("whyCont").scrollIntoView({ behavior: "smooth" });
}
</script>

<template>
  <div>
    <section class="splashCont">
      <span>STOP THE 413</span>
      <div @click="learnClick" class="cta">Learn Why</div>
    </section>
    <video @click="playVid" id="bgVid" autoplay muted loop src="../assets/bg_1.mp4"></video>
  </div>
</template>

<style lang="scss" scoped>
.splashCont {
  width: 100%;
  height: 100vh;
  position: relative;
  top: 0px;
  left: 0px;
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--light);
  background: url("../assets/dust.jpg");
  animation: bg 0.5s infinite linear alternate-reverse;
  background-size: cover;
  mix-blend-mode: screen;
  flex-direction: column;
  backdrop-filter: blur(5px);

  span {
    font-family: var(--customFont);
    font-weight: 900;
    font-size: 20vh;
    line-height: 20vh;
    text-align: center;
    padding: 10px;
    z-index: 5;
  }
}

@keyframes bg {
  0% {
    background: url("../assets/dust.jpg");
  }

  50% {
    background: url("../assets/dust2.jpg");
  }

  100% {
    background: url("../assets/dust3.jpg");
  }
}

.cta {
  font-size: 3vh;
  padding: 10px 20px;
  border: solid 2px var(--light);
  margin: 20px;
  transition: all 0.3s ease;
  font-weight: bold;
  cursor: pointer;

  &:hover {
    color: var(--dark);
    background: var(--highlight);
    border: solid 2px var(--highlight);
    padding: 10px 30px;
  }
}

#bgVid {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  object-fit: cover;
  z-index: -1;
  filter: brightness(0.5);
}
</style>
