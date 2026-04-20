<script setup>
//부모 컴포넌트에서 자식 컴포넌트로 데이터를 전달하는 사용자 정의 속성
// 기본 Readonly, 단반향 데이터 바인딩을 형성
import{ref} from'vue';
import PropsChild from './PropsChild.vue';

const cnt = ref(0);
// Component Event 컴포넌트 이벤트 : 
//`$emit` 메소드를 사용해서 부모 컴포넌트와 자식 컴포넌트 간에 에벤트를 수신 or발신
// 부모 컨테이너는 `v-on`을 사용하여수신
//`@이벤트명-"실행할js코드"` 자식컴포넌트태그속성으로추가
//자식 컴포넌트에서는 `$emit(이벤트명)`으로 발신
//-아규먼트가 복수일 경우 가변 파라미터로 작성 `$emit('이벤트명'[,...아규먼트])`

function minusCnt(num) {
  cnt.value-=num;
}
</script>

<template>
<h1>프롭스: {{cnt}}</h1>

<button type="button" @click="cnt++">증가(부모쪽)</button>
<!--  자식 컴포넌트에 `:키명="값"` 으로 이루어진 props속성을 부여 -->

<PropsChild :cnt="cnt" :page="1" @minusCnt="minusCnt"/>


</template>

<style scoped>

</style>