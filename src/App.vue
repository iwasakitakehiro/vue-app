<script setup>
import { ref } from "vue";
import firsCompornent from "./components/firstCompornent.vue";
import second from "./components/second.vue";
import thrid from "./components/third.vue";
import Input from "./components/Input.vue";

const name = ref("name");

const handleEvent = (newName) => {
  name.value = newName;
};
</script>

<template>
  <!-- <firsCompornent /> -->
  <!-- <second :name="name" message="propsの使用" /> -->
  <thrid :changeNameEvent="handleEvent" :name="name" />
  <!-- <h1>入力フォーム</h1>
  <p>{{ name }}</p>
  <Input v-model="name" />
  <p>{{ address }}</p>
  <Input :model-value="address" @update:model-value="address = $event" /> -->
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
