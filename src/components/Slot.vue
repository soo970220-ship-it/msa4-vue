<script setup>

import{ref} from'vue';
import SlotChild from './SlotChild.vue';

const cnt = ref(0);
const cnt2=0;
</script>

<template>
  <h1>슬롯</h1>
  <button type="button" @click="()=>{cnt2++;console.log(cnt2);}">cnt++
  </button>
  
  <SlotChild>
  <div>
    <h2>보내줄 슬롯: {{ cnt }}</h2>
    <h3>dkdkd{{ cnt2 }}</h3>
  </div>  
   </SlotChild>
  
</template>

<style scoped>

</style>