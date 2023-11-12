<template>
  <div>
    <div class="text-h5 text-center text-weight-bold q-mb-xl">비밀번호 찾기</div>
    <q-form class="q-gutter-y-md">
      <q-input placeholder="가입한 이메일" outlined dense/>

      <q-btn label="확인"
             class="full-width"
             unelevated
             color="primary"

      />
    </q-form>
  </div>
</template>

<script setup lang="ts">
defineEmits(['changeView']);
</script>
