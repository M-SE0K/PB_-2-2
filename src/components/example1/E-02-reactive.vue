<template>
  <div>{{ fullName }}</div>
</template>

<script setup lang="ts">
import { ref, computed, onMounted } from 'vue';

const firstName = ref("Minseok");
const lastName = ref("Kwon");

const fullName = computed(() => firstName.value + " " + lastName.value);

onMounted(() => {
  setTimeout(() => {
    firstName.value = "KMS";
  }, 2000);
});
</script>
