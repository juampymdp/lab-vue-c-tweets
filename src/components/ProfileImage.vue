
<script setup>
defineProps({
  image: {
    type: String,
    required: true
  }
});
</script>

<template>
  <img :src="image" alt="Profile Image" class="profile" />
</template>

<style scoped>
.profile {
  width: 48px;
  height: 48px;
  border-radius: 50%;
}
</style>
