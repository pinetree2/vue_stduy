
<template>
    <div>
    <h1>해송이의 컴포넌트</h1>
    <h2>{{ message }}</h2>
    <ul>
        <button @click="increment">Count is: {{ count }}</button>
        <button @click="getPosts">데이터 모으기</button>
        <li v-for="post in posts" :key ="post.id">
        {{ post.title }}</li>

    </ul>

 
</div>
</template>

<script>
import { ref, onMounted } from 'vue'
import axios from 'axios'
// reactive state
const count = ref(0)
// functions that mutate state and trigger updates
function increment() {
  count.value++
}
// lifecycle hooks
onMounted(() => {
  console.log(`The initial count is ${count.value}.`)
})


 
export default{
    name: 'MyComponent',
    
    data : function(){
        return{
            message :'해송이의 Mycomponent.vue에서 보내는 메시지',
            posts:[]
            
        }
    },

    data() {
    return {
      count: 0
    }
    },

    methods: {
        //axios get
        getPosts: function() {
            axios.get('https://koreanjson.com/posts')
                .then(res => this.posts = res.data)
        },
        increment() {
        this.count++
    }
    },


  mounted() {
    console.log(`The initial count is ${this.count}.`)
  }


  

}
</script>

<style>
</style>
