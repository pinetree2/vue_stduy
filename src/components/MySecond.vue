

<template>
    <div>
    <h1>{{ msg }}</h1>
    </div>

    <div class="menu">
      <!-- 자료안의 데이터 갯수만큼 반복됨, 그때 index(작명한 변수)는 데이터 안의 자료가 됨
      변수 작명 2개 까지 가능하다.
      v-for(a,i) in products 이런식으로.
      - 왼쪽 변수는 array 내의 데이터
      - 오른쪽 변수는 1 씩 증가하는 정수
      -->
      <a v-for="index in menus" :key="index">{{ index }}</a>

      <!--key ="" 의 용도는 반복문 쓸때 꼭 써야한다. 반복문 돌린 요소를 컴퓨터가 구분하기 위해 씀
      
      <h4 v-for="(rooms,index) in room" :key="rooms">
      <h4>{{index+1 }}</h4>    
      <h4>{{ rooms }}</h4>
      <h3>{{ rooms[index] }}</h3>
    </h4>
      
      -->
  </div>
  <div>
    
    <h4 v-for="rooms in products" :key="rooms">
      <h3>{{ rooms.room }}</h3>
      <h3>{{ rooms.prices }}</h3>

    </h4>
  </div>


<!--

    <div>
    <h4>{{products[0]}}</h4>
    <p>50만원</p>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>60만원</p>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>70만원</p>
  </div>
-->

</template>

<script>

export default {
  name: 'App',
  props: {
    msg: String
  },
  data(){
      return {
          menus:['Home','Shop','About'],
          products :[{ room :'역곡동 원룸', prices:'50만원'}, 
          {room: '천호동 원룸',prices:'60만원'},
          {room: '마포구 원룸',prices: '70만원'}]
      }
      
  }

}
</script>

<style>

  #app{
    font-family: Avenir,Arial, Helvetica, sans-serif;
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    text-align:center;
    color: #2c3e50;
  }

  .menu {
  background : darkslateblue;
  padding : 15px;
  border-radius : 5px;
}
.menu a {
  color : white;
  padding : 10px;
}

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}





</style>
