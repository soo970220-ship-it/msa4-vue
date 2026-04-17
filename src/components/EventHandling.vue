<script setup>
import {ref} from 'vue';

const cnt = ref(0);
let test=ref(0);

test.value=1;

function resetCnt(){
    cnt.value = 0;
 }
</script>

<template>
<h1>이벤트 핸들링: {{ cnt }}</h1>
<button type="button" @mousemove="cnt++">인라인 핸들러</button>
<button type="button" @click="resetCnt(9)">메소드 핸들러</button>
<input type="text" @keydown="cnt++" v-model="cnt">
</template>

<style>

</style>