<script setup>
import { ref } from "vue";
import firsCompornent from "./components/firstCompornent.vue";
import second from "./components/second.vue";
import thrid from "./components/third.vue";

const name = ref("jhon");

const handleEvent = (newName) => {
  name.value = newName;
};
</script>

<template>
  <!-- <firsCompornent /> -->
  <!-- <second :name="name" message="propsの使用" /> -->
  <thrid @changeNameEvent="handleEvent" :name="name" />
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
