<template>
  <q-page padding>
    <div class="row q-col-gutter-x-lg">
      <PostLeftBar class="col-grow"/>
      <section class="col-7">
        <PostHeader/>

        <PostList :items="posts"/>
      </section>
      <PostRightBar class="col-3"/>
    </div>

  </q-page>
</template>

<script setup lang="ts">
import PostList from 'components/apps/post/PostList.vue';
import PostLeftBar from 'pages/components/PostLeftBar.vue';
import PostRightBar from 'pages/components/PostRightBar.vue';
import PostHeader from 'pages/components/PostHeader.vue';


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
