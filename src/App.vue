<template>
  <div id="app">
    <h1>Vue Tweets</h1>
    <TweetList :tweets="tweets" />
  </div>
</template>

<script>
import { ref } from 'vue';
import TweetList from './components/TweetList.vue';

export default {
  name: 'App',
  components: {
    TweetList
  },
  setup() {
    const tweets = ref([
      {
        id: 1,
        user: {
          name: 'Juan Pérez',
          handle: 'juanperez',
          avatar: 'https://i.pravatar.cc/48?img=1'
        },
        content: '¡Hola mundo! Este es mi primer tweet.',
        likes: 10,
        retweets: 2
      },
      {
        id: 2,
        user: {
          name: 'María García',
          handle: 'mariagarcia',
          avatar: 'https://i.pravatar.cc/48?img=2'
        },
        content: 'Vue.js es increíble. ¡Me encanta!',
        likes: 25,
        retweets: 5
      }
    ]);

    return {
      tweets
    };
  }
};
</script>

<style>
#app {
  max-width: 600px;
  margin: 2rem auto;
  font-family: 'Helvetica Neue', Arial, sans-serif;
}
h1 {
  text-align: center;
  margin-bottom: 2rem;
}
</style>
