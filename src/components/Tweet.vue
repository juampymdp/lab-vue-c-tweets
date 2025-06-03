<template>
  <div class="tweet">
    <div class="tweet-header">
      <img :src="tweet.user.avatar" alt="Avatar" class="avatar" />
      <div class="user-info">
        <strong>{{ tweet.user.name }}</strong>
        <span>@{{ tweet.user.handle }}</span>
      </div>
    </div>
    <p class="tweet-content">{{ tweet.content }}</p>
    <div class="tweet-footer">
      <span>{{ tweet.likes }} Likes</span>
      <span>{{ tweet.retweets }} Retweets</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tweet',
  props: {
    tweet: {
      type: Object,
      required: true
    }
  }
};
</script>

<style scoped>
.tweet {
  border: 1px solid #e1e8ed;
  padding: 1rem;
  margin-bottom: 1rem;
  border-radius: 8px;
  background-color: #fff;
}
.tweet-header {
  display: flex;
  align-items: center;
}
.avatar {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  margin-right: 0.5rem;
}
.user-info {
  display: flex;
  flex-direction: column;
}
.tweet-content {
  margin: 1rem 0;
}
.tweet-footer {
  display: flex;
  justify-content: space-between;
  font-size: 0.9rem;
  color: #657786;
}
</style>
