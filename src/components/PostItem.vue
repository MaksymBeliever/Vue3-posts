<template>
  <div class="post">
    <div><strong>Name:</strong> {{ post.title }}</div>
    <div><strong>Description:</strong> {{ post.body }}</div>
  </div>
</template>

<script>
export default {
  name: 'PostItem',
  props: {
    post: Object,
    required: true
  }
}
</script>

<style scoped>
  .post {
    margin-top: 15px;
    padding: 15px;
    border: 2px solid teal;
  }
</style>
