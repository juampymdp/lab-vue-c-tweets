<template>
  <div>
    <Tweet v-for="tweet in tweets" :key="tweet.id" :tweet="tweet" />
  </div>
</template>

<script>
import Tweet from './Tweet.vue';

export default {
  name: 'TweetList',
  components: {
    Tweet
  },
  props: {
    tweets: {
      type: Array,
      required: true
    }
  }
};
</script>
