<script setup>
import{ref,emit} from "vue"
const userList=ref([]);
fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
      .then(json => userList.value=json)
console.log(userList);

const showDetail=(user)=>{
emit('user-selected',user)
}

</script>

<template>
<ul v-for="user in userList" :key="user.id">
	<li @click="showDetail(user)">
		<a >{{user.name}}</a>
		</li>
</ul>

</template>