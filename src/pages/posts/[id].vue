<script setup lang="ts">
import {useRoute} from 'vue-router';

let route = useRoute();
</script>

<template>
  <q-page padding>
    <div class="text-h4">Posts/[id].vue</div>
    <div>{{route}}</div>
  </q-page>
</template>

<route lang="yaml">
meta:
  width: 600px
</route>
