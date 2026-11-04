<script setup>
import { ref } from 'vue';
//데이터 바인딩을 해주는 객체 = ref(); 
const count = ref(0);
const bgColor = ref('');
const email = ref('abc');


const plus = ()=>{
    count.value++;
}
const reset = ()=>{
    count.value = 0;
}
const minus = ()=>{
    if(count.value >0){
        count.value--;
    }
}

const toggleBgColor = ()=>{
    if(bgColor.value === ''){
        bgColor.value = 'bg-red';
    }else{
        bgColor.value ='';
    }
}
</script>
<template>
    <div @click="plus" class="btn-cnt" :class="bgColor">Count is {{ count }}</div>
    <button @click="reset">reset</button>
    <button @click = "minus">Count Down</button>
    <button @click="bgColor = 'bg-red'" class="red">빨간색버튼</button>

    <button @click="toggleBgColor">Toggle</button>
    <br><br>

    <input type="text" name="email" id="email" v-model="email">
    {{ email }}
</template>
<style>
.btn-cnt{  
    width: 100px;
    height: 100px;
    background-color: cadetblue;
    border: solid 1px #555;
    display: flex;
    align-items: center;
    justify-content: center;
}

.bg-red{
    background-color: red;
}

</style>