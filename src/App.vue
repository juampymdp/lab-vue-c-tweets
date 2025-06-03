<script setup>
import { ref } from 'vue';
import TweetList from './components/TweetList.vue';

const tweets = ref([
  {
    id: 1,
    user: {
      name: 'Juan Pérez',
      handle: 'juanperez',
      image: 'https://i.pravatar.cc/48?img=1'
    },
    message: '¡Hola mundo! Este es mi primer tweet.',
    timestamp: '2025-06-02 10:24:00'
  },
  {
    id: 2,
    user: {
      name: 'María García',
      handle: 'mariagarcia',
      image: 'https://i.pravatar.cc/48?img=2'
    },
    message: 'Vue.js es increíble. ¡Me encanta!',
    timestamp: '2025-06-02 10:30:00'
  },
  {
    id: 3,
    user: {
      name: 'Carlos Rivera',
      handle: 'carlosr',
      image: 'https://i.pravatar.cc/48?img=3'
    },
    message: 'Estoy aprendiendo Vue con Ironhack 💪',
    timestamp: '2025-06-02 11:00:00'
  }
]);
</script>

<template>
  <div id="app">
    <h1>Vue Tweets</h1>
    <TweetList :tweets="tweets" />
  </div>
</template>

<style scoped>
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
