<script setup>
import { ref } from "vue";
var fontsReady = ref(false);

document.fonts.ready.then(
  setTimeout(() => {
    fontsReady.value = true;
  }, 1000)
);
</script>

<template>
  <div v-if="!fontsReady" class="loadingCont"></div>
</template>

<style lang="scss" scoped>
.loadingCont {
  position: fixed;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  background: rgba($color: #000000, $alpha: 0.5);
  z-index: 100;
}
</style>
