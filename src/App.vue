<script setup>
import { RouterView } from "vue-router";
import NavigationBar from "./components/layouts/NavigationBar.vue";
</script>

<template>
  <NavigationBar />

  <RouterView />
</template>

<style>
@import "@/assets/css/styles.css";

</style>
