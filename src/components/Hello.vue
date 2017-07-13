<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
      <router-link to="/about">About Page</router-link>
      <Comment ref="comment"></Comment>
  </div>
</template>

<script>
import Comment from '@/components/Comment';

export default {

  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    Comment,
  }
}
</script>
