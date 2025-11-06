<!-- ParentComponent.vue -->
<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        @custom-event="handleEvent"
    />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import ChildComponent from './ChildComponent.vue';

const parentMessage = ref('Hello from parent');

const handleEvent = (payload: any) => {
  console.log(payload);
};
</script>
