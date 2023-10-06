<template>
  <div class="app">
    <PostForm @create="createPost" />
    <PostList :posts="posts" />
  </div>
</template>

<script>
import PostList from '@/components/PostList.vue';
import PostForm from '@/components/PostForm.vue';
  export default {
    components: {
      PostForm,
      PostList,
    },
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
      createPost(post) {
        this.posts.push(post);
      }
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  .app {
    padding: 20px;
  }
</style>
