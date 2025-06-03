<script setup>
defineProps({
  message: {
    type: String,
    required: true
  }
});
</script>

<template>
  <p class="message">{{ message }}</p>
</template>

<style scoped>
.message {
  margin: 10px 0;
}
</style>