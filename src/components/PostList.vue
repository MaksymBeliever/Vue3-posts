<template>
  <PostItem v-for="post of posts" :key="post.id" :post="post" />
</template>

<script>
import PostItem from '@/components/PostItem.vue';

export default {
  name: 'PostList',
  components: { PostItem },
  props: {
    posts: Array,
    required: true,
  },
}
</script>

<style scoped>

</style>
