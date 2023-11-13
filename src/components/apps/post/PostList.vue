<template>
  <q-list bordered separator>
    <PostItem v-for="post in items" :key="post.id"
              v-bind="post"
    />
  </q-list>
</template>

<script setup lang="ts">
import {Post} from 'components/apps/post/post';
import PostItem from 'components/apps/post/PostItem.vue';

defineProps({
  items: {
    type: Array<Post>,
    default: () => [],
  }
});
</script>
