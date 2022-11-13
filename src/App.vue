<script setup lang="ts"></script>

<template>
  <img
    alt="Vue logo"
    class="logo logo1"
    src="@/assets/logo.svg"
    width="125"
    cy-data="logo1"
  />
  <img
    alt="Vue logo"
    class="logo logo2"
    src="@/assets/logo.svg"
    width="125"
    data-cy="logo2"
  />
</template>

<style scoped>
.logo {
  position: absolute;
}
.logo1 {
  transform: translateX(100px) rotate(45deg);
}
.logo2 {
  transform: rotate(45deg) translateX(100px);
}
</style>
