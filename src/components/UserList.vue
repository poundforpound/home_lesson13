<script setup>
import{ref} from "vue"
const userList=ref([]);
fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
      .then(json => userList.value=json)
console.log(userList);

function showDetail(user) {
  emit('user-selected', user);
}

</script>

<template>
<div>
	<ul v-for="user in userList" :key="user.id">
		<li @click="showDetail(user)">
			<a >{{user.name}}</a>
			</li>
	</ul>
	<UserDetails v-if=""/>
</div>
</template>