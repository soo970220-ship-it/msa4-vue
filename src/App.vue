<script setup>
import DataBinding from './components/DataBinding.vue';
import EventHandling from './components/EventHandling.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRandering from './components/ListRandering.vue';
import Watchers from './components/Watchers.vue';
import Props from './components/Props.vue';
import Slot from './components/Slot.vue';
import MyTransition from './components/MyTransition.vue';
import LifeCycle from './components/LifeCycle.vue';

// js코드작성부분 

</script>

<template>
<!-- HTML 작성부분 -->
<!-- 조건부 랜더링 -->
   <DataBinding v-if="false"/>  
   <EventHandling v-if="false"/>
   <ConditionalRendering v-if="false"/>
   <ListRandering v-if="false"/>
   <Watchers v-if="false"/>
   <Props v-if="false"/>
   <Slot v-if="false"/>
   <MyTransition v-if="false"/>
   <LifeCycle/>
   <button type="button" @click="flgLifeCycle=!flgLifeCycle"> 라이프사이클 컴포넌트 토글</button>

</template>

<style>
/* CSS작성부분 */
</style>