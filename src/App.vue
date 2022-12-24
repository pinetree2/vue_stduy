
<script setup>
import MySecond from './components/MySecond.vue'
import MyThird from './components/ThirdComponent.vue'
</script>
<template>

  <!-- [Vue 컴포넌트 객체 생성 시 초기화할 데이터 및 메시지 설정] -->

  <img alt="Vue logo" src="./assets/logo.svg"> 

  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  
  <div class="wrapper">
    <MySecond msg="MainComponent"/>
    <MyThird></MyThird>
  </div>


</template>



<style>
#app {
  width: 100%;
  height: 100%;
  margin: 0 auto;
  padding: 0;
  border: none;

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;  
}





#main {
  width: 100%;
  height: 100%;
  margin: 0 auto;
  padding: 0;
  border: none;

  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;  
}
</style>
