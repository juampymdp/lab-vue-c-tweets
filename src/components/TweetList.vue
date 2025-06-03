<script setup>
import Tweet from './Tweet.vue';

defineProps({
  tweets: {
    type: Array,
    required: true
  }
});
</script>

<template>
  <div>
    <Tweet v-for="tweet in tweets" :key="tweet.id" :tweet="tweet" />
  </div>
</template>