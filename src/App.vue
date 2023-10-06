<template>
  <div class="app">
    <form class="form" @submit.prevent>
      <h4>Create post</h4>
      <input
          v-model="title"
          class="input"
          type="text"
          placeholder="name"
      >
      <input
          v-model="body"
          class="input"
          type="text"
          placeholder="description"
      >
      <button class="btn" @click="createPost">Create</button>
    </form>
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
        title: '',
        body: '',
      }
    },
    methods: {
      createPost() {
        const newPost = {
          id: Date.now(),
          title: this.title,
          body: this.body,
        };

        this.posts.push(newPost);
        this.title = '';
        this.body = '';
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

  .post {
    margin-top: 15px;
    padding: 15px;
    border: 2px solid teal;
  }

  .btn {
    margin-top: 15px;
    align-self: end;
    padding: 10px 15px;
    background: none;
    color: teal;
    border: 1px solid teal;
  }

  .form {
    display: flex;
    flex-direction: column;
  }

  .input {
    width: 100%;
    border: 1px solid teal;
    padding: 10px 15px;
    margin-top: 15px;
  }
</style>
