

<template>
  <q-page padding>
    <div class="text-h4">커뮤니티 목록</div>
    <section class="q-gutter-y-sm q-mt-lg">
     <PostList :items="posts"/>
    </section>

  </q-page>
</template>

<script setup lang="ts">
import PostList from 'components/apps/post/PostList.vue';

const posts = Array.from(Array(20), (_, index) => ({
  id: index,
  title: `Vue3 Firebase 강의 ${index}`,
  content: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. A aspernatur at aut deserunt dolorem enim explicabo facere impedit libero molestiae mollitia nihil non odio placeat possimus, tempore ullam velit voluptatum?`,
  readCount: 3,
  likeCount: 4,
  bookmarkCount: 10,
  tags: ['html', 'css', 'javascript'],
  uid: 'uid',
  category: '카테고리' + index,
}));

</script>
