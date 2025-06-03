
<script setup>
defineProps({
  userData: {
    type: Object,
    required: true
  }
});
</script>

<template>
  <span class="user">
    <span class="name">{{ userData.name }}</span>
    <span class="handle">@{{ userData.handle }}</span>
  </span>
</template>

<style scoped>
.user {
  font-weight: bold;
}
.name {
  margin-right: 5px;
}
.handle {
  color: #657786;
}
</style>
