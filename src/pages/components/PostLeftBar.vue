<template>
  <StickySideBar>
    <q-card flat bordered>
      <q-list>
        <q-item :active="true">
          <q-item-section>전체</q-item-section>
        </q-item>
        <q-item v-for="category in categories" :key="category.value" clickable v-ripple>
          <q-item-section>
            {{ category.label }}
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>
  </StickySideBar>

</template>

<script setup lang="ts">
import StickySideBar from 'components/StickySideBar.vue';

const categories = [
  {
    label: 'Q&A',
    value: 'qna',
  },
  {
    label: '커뮤니티',
    value: 'comunity',
  },
  {
    label: '공지사항',
    value: 'notice',
  },
  {
    label: '강의',
    value: 'lecture ',
  },
]
</script>
