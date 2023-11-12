<script setup lang="ts">
import {ref} from 'vue';
import {useRoute} from 'vue-router';
const route = useRoute();

const pageContainerStyles = ref({
  maxWidth: route.meta.width || '1080px',
  margin: '0 auto',
});

</script>

<template>
  <q-layout view="hHh lpR fFf" class="bg-grey-4">

    <q-header bordered class="bg-white text-grey-9">
      <q-toolbar>
        <q-btn flat dense to="/">
          <q-toolbar-title>
            <q-avatar>
              <img src="favicon.ico">
            </q-avatar>
            동성코딩클럽
          </q-toolbar-title>
        </q-btn>

        <q-space/>

        <q-btn stretch
               flat
               label="Home"
               to="home"
        />
        <q-btn stretch
               flat
               label="수강하기" href="https://www.google.co.kr" target="_blank"/>
        <q-btn stretch
               flat
               label="온라인 강의"/>
        <q-btn stretch
               flat
               label="유튜브"/>

        <q-separator class="q-my-md q-mr-md" vertical/>
        <q-btn unelevated rounded color="primary" label="로그인 / 회원가입"/>

      </q-toolbar>
    </q-header>

    <q-page-container :style="pageContainerStyles">
      <router-view/>
    </q-page-container>

  </q-layout>
</template>
