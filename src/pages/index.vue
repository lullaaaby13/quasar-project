

<template>
  <q-page padding>
    <div class="text-h4">커뮤니티 목록</div>
    <section class="q-gutter-y-sm q-mt-lg">
      <q-card
        class="cursor-pointer"
        v-for="index in 100" :key="index"
        @click="goPostDetails(index)">
        <router-link :to="`/posts/${index}`">
          <q-card-section>{{ index }}게시글</q-card-section>
        </router-link>
      </q-card>
    </section>
  </q-page>
</template>

<script setup lang="ts">

import {useRouter} from 'vue-router';

const router = useRouter();
const goPostDetails = (id: number) => router.push(`/posts/${id}`);
</script>
