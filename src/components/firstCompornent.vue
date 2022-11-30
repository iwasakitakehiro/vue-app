<script setup>
import { ref, computed, reactive } from "vue";

const count = ref(0);
const user = reactive({
  firstName: "jhon",
  lastName: "Doe",
});
const fullName = computed({
  get() {
    return `${user.firstName} ${user.lastName}`;
  },
  set(newValue) {
    const names = newValue.split(" ");
    user.firstName = names[0];
    user.lastName = names[names.length - 1];
  },
});
const fFullName = () => {
  return ` ${user.firstName} ${user.lastName}`;
};

const changeName = () => {
  fullName.value = "jhon Doe";
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
    <button @click="changeName">名前を変更する</button>
  </div>
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
