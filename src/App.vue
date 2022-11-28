<script setup>
import { ref } from "vue";
let message = "hello world";
const message1 = "<div><h1>Hello World</h1></div>";
const link = "https://google.com";
const upperCase = () => {
  message = message.toUpperCase();
};
let isActive = true;
let isBlack = true;
let empty = false;
upperCase();
const count = ref(0);
const countUp = () => {
  count.value += 1;
};
</script>

<template>
  <h1>Vue 3 入門</h1>
  <p>{{ message.length > 20 ? "Long" : "Short" }}</p>
  <p v-text="message"></p>
  <p v-html="message1"></p>
  <a v-bind:href="link">Google</a>
  <div>
    <a v-bind:class="[isActive ? 'active' : 'underLine']">v-bindの設定方法</a>
  </div>
  <div>
    <p v-if="empty">品切れ中です</p>
    <p v-else>好評販売中！</p>
  </div>
  <div>
    <button type="button" @click="countUp">+</button>
    <div>
      <p>{{ count }}</p>
    </div>
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
