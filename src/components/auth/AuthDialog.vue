<template>
  <q-dialog :model-value="modelValue"
            @update:model-value="val => $emit('update:modelValue', val)"
            transition-show="none"
            transition-hide="none"
  >
    <q-card style="width: 400px;">
      <q-card-section class="flex justify-end">
        <q-btn flat
               round
               dense
               icon="close"
               v-close-popup
        />
      </q-card-section>

      <q-card-section class="q-px-xl q-pb-xl">
        <SignInForm v-if="viewMode === 'SignInForm'"
                    @change-view="changeViewMode"
        />
        <SignUpForm v-else-if="viewMode === 'SignUpForm'"
                    @change-view="changeViewMode"
        />
        <FindPasswordForm v-else
                    @change-view="changeViewMode"
        />
      </q-card-section>

    </q-card>
  </q-dialog>
</template>

<script setup lang="ts">
import SignInForm from 'components/auth/SignInForm.vue';
import SignUpForm from 'components/auth/SignUpForm.vue';
import FindPasswordForm from 'components/auth/FindPasswordForm.vue';
import {ref} from 'vue';

defineProps({
  modelValue: {
    type: Boolean,
    default: false,
  },
});

defineEmits(['update:modelValue']);

const viewMode = ref('SignInForm');
const changeViewMode = (mode: string) => viewMode.value = mode;

</script>
