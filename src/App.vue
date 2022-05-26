<script setup>
import { ref, reactive } from "vue";
import Splash from "./components/Splash.vue";
import Why from "./components/Why.vue";
import Loading from "./components/Loading.vue";
</script>

<template>
  <Splash />
  <Why />
  <Loading />
</template>

<style lang="scss">
:root {
  --light: #ffffff;
  --dark: #0e3e4c;
  --secondary: #236264;
  --highlight: #fbed25;
  --lowlight: #66a789;
  --customFont: Nothing You Could Do;
}

body,
html {
  padding: 0px;
  margin: 0px;
  font-family: Open Sans, Arial, Helvetica, sans-serif;
}
</style>
