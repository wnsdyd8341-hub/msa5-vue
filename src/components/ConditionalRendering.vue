<script setup>
import { ref } from 'vue';

    const num = ref(0);
    const flg = ref(true);
</script>   
<template>
<!-- 조건부 렌더링 -->
    <input type="number" v-model="num">
    
    <!-- v-if 는 조건문  -->
    <p v-if="num%2==0">짝수입니다</p>
    <p v-else="num%2==1">홀수입니다</p>
    <hr>
    <!-- 부여하고싶은 스타일명 : 이 조건일때 부여 -->
    <button :class="{'btn-toggle': flg ===false}" @click="flg = !flg">토글</button>
    
    <!-- v-if는 아예 요소를 삭제하는거라 , Dom을 유지안한다 -->
    <p v-if = "flg">v-if</p>
    <!-- v-show는 display :none으로 해서 안보여준다 , Dom을 유지 -->
    <p v-show = "flg">v-show</p>
</template>
<style>
.btn-toggle{
    background-color: #5f9ea0;
}
</style>