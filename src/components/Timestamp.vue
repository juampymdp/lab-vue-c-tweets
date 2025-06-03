<script setup>
defineProps({
  time: {
    type: String,
    required: true
  }
});
</script>


<template>
  <span class="timestamp">{{ time }}</span>
</template>

<style scoped>
.timestamp {
  color: #657786;
  margin-left: 10px;
  font-size: 0.85rem;
}
</style>