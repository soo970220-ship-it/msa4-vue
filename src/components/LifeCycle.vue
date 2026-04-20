<script setup>
import { onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated, ref } from 'vue';

const cnt = ref(0);

onBeforeMount(() => {
  console.log('onBeforeMount', cnt.value);
});

onMounted(() => {
  cnt.value++;
  console.log('onMounted', cnt.value);
});

onBeforeUpdate(() => {
  console.log('onBeforeUpdate', cnt.value);
});

onUpdated(() => {
  console.log('onUpdated', cnt.value);
});

onBeforeUnmount(() => {
  console.log('onBeforeUnmount', cnt.value);
});

onUnmounted(() => {
  console.log('onUnmounted', cnt.value);
});
</script>

<template>
 <h1>라이프 사이클: {{ cnt }}</h1>
 <button type="button" @click="cnt++">증가</button>
</template>

<style>

</style>