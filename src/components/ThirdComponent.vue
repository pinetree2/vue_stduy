
<template>
    <div>
      <h1>사용자</h1>
  
      <ul v-for="item in users" :key="item">
          <li>이름 : {{ item.id }} </li>
          <li>전화번호 : {{ item.phone_number }}</li>
          <li>등록 시간 :{{ item.created_date  }} </li>
      </ul>    
    </div>
  </template>
<script>
import axios from 'axios';
import userList from "@/test.json";

export default {
    name: "UserList",
  computed: {
    users() { // #1
      return userList.users.map((items) => { // #2
        // #3 
          let c = new Date(items["created_date"]); 
          let created_date = c.getHours()+"시 "+c.getMinutes()+"분"; 

          items["created_date"] = created_date;
          
        return items;
      })
    },
  }
}
</script>

<style>

</style>