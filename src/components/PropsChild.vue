<script setup>

//자식 컴포넌트에서는 defineProps() 이용해 넘어온 데이터 선언
// - 이때 부모 컴포넌트에서 넘겨줄 때 사용한 키를 사용해 선언
// -데이터 타입도 지정
defineProps(['cnt', 'page']);

//  defineProps({ 
//   'cnt' : Number,
//   'page' : Number'
//    });

//자식 컴포넌트에서는 defineEmits()디파인에밋을 이용해 넘어온 컴포넌트 이벤트 선언
// 이때 부모 컴포넌트에서 넘겨줄 때 사용한 이벤트 명을 사용해 선언
//const emit = defineEmits(['minusCnt']);
defineEmits(['minusCnt']);
</script>

<template>
<h1>{{page}}프롭스 자식 컴포넌트: {{cnt }}</h1>
<button type="button" @click="$emit('minusCnt', 10)">감소(자식쪽)</button>
<!-- 명시적으로 썻을땐 달러($)가 빠저야한다 -->
</template>

<style scoped>

</style>