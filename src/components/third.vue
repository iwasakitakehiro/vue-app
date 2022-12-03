<script setup>
import { ref } from "vue";
const props = defineProps({
  name: String,
});
const emit = defineEmits(["changeNameEvent"]);
</script>
<template>
  <h2>子コンポーネント</h2>
  <p>Hello {{ name }}</p>
  <input type="text" @input="$emit('changeNameEvent', $event.target.value)" />
</template>
