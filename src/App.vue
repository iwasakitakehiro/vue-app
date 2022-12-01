<script setup>
import { ref } from "vue";
import firsCompornent from "./components/firstCompornent.vue";
import second from "./components/second.vue";

const name = ref("");
</script>

<template>
  <!-- <firsCompornent /> -->
  <input type="text" v-model="name" />
  <second :name="name" message="propsの使用" />
</template>

<style scoped>
.active {
  color: red;
}
.black {
  color: black;
}
.underLine {
  text-decoration: underline;
}
</style>
