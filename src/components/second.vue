<script setup>
const { name, message } = defineProps({
  message: String,
  name: { type: String, default: "Jhon" },
});
</script>
<template>
  <div>
    <p>{{ message }}</p>
    <p>{{ name }}</p>
  </div>
</template>
