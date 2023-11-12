<template>
  <q-page padding>
    <div class="text-h4">Home</div>
    <section class="q-gutter-y-sm q-mt-lg">
      <q-card v-for="index in 100" :key="index">
        <q-card-section>{{ index }}게시글</q-card-section>
      </q-card>
    </section>
  </q-page>
</template>

<route lang="yaml">
meta:
  width: 600px
</route>
