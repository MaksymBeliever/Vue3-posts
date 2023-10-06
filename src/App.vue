<template>
  <div>
    <div class="post" v-for="post of posts" :key="post.id">
      <div><strong>Name:</strong> {{ post.title }}</div>
      <div><strong>Description:</strong> {{ post.body }}</div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        posts: [
          { id: 1, title: 'JavaScript', body: 'description' },
          { id: 2, title: 'TypeScript', body: 'description' },
          { id: 3, title: 'Vue', body: 'description' },
          { id: 4, title: 'React', body: 'description' },
        ],
      }
    },
    methods: {

    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .post {
    margin-top: 15px;
    padding: 15px;
    border: 2px solid teal;
  }
</style>
