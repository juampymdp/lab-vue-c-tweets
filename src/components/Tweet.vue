<script setup>
import ProfileImage from './ProfileImage.vue';
import User from './User.vue';
import Timestamp from './Timestamp.vue';
import Message from './Message.vue';
import Actions from './Actions.vue';

defineProps({
  tweet: {
    type: Object,
    required: true
  }
});
</script>


<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />
    <div class="body">
      <div class="top">
        <User :userData="tweet.user" />
        <Timestamp :time="tweet.timestamp" />
      </div>
      <Message :message="tweet.message" />
      <Actions />
    </div>
  </div>
</template>

<style scoped>
.tweet {
  display: flex;
  align-items: flex-start;
  gap: 1rem;
  border-bottom: 1px solid #e1e8ed;
  padding: 1rem 0;
}
.body {
  flex: 1;
}
.top {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
</style>

