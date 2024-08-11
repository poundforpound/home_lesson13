//UserList
<script setup>
import{ref} from "vue"
import UserDetail from './UserDetail.vue';
const userList=ref([]);
fetch('https://jsonplaceholder.typicode.com/users')
      .then(response => response.json())
      .then(json => userList.value=json)

const currentUser = ref(null)

</script>

<template>
<div>
	<ul v-for="user in userList" :key="user.id">
		<li @click="currentUser=user">
			<a >{{user.name}}</a>
			</li>
	</ul>
	<UserDetail v-if="currentUser" :user="currentUser"/>
</div>
</template>