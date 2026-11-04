<script setup>
import { ref } from 'vue';

    const name = ref('');
</script>   
<template>
    <h2>TabUI</h2>
    <div>
        <button :class="{'color' : name ==='프로필'}" @click="name = '프로필'">프로필</button>
        <button :class="{'color' : name ==='설정'}" @click="name = '설정'">설정</button>
        <button :class="{'color' : name ==='게시판'}" @click="name = '게시판'">게시판</button>
    </div>    

    <p>{{ name }} 페이지 입니다</p>
</template>
<style>
    div{
        display: flex;
        align-items: center;
    }
    button{
        padding: 10px;
    }
    .color{
        color: blue;
        background-color: #fff;
        border-bottom: solid 3px blue;
    }
</style>