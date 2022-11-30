<script setup>
import { ref } from "vue";
import { reactive } from "vue";
import { computed } from "vue";

const count = ref(0);

const user = reactive({
  firstName: "jhon",
  lastName: "Doe",
});
const fullName = computed(() => {
  console.log("computed Propety");
  return `${Math.random()} ${user.firstName} ${user.lastName}`;
});
const fFullName = () => {
  console.log("function");
  return `${Math.random()} ${user.firstName} ${user.lastName}`;
};
</script>

<template>
  <h1>Vue 3 基本的な記述</h1>
  <input v-model="user.firstName" />
  <input v-model="user.lastName" />
  <h2>fullName: {{ user.firstName }} {{ user.lastName }}</h2>
  <h2>fFullName: {{ fFullName() }}</h2>
  <h2>fFullName: {{ fFullName() }}</h2>
  <h2>fFullName: {{ fFullName() }}</h2>
  <h2>fullName: {{ fullName }}</h2>
  <h2>fullName: {{ fullName }}</h2>
  <h2>fullName: {{ fullName }}</h2>
  <div>
    <button @click="count++">{{ count }}</button>
  </div>
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
