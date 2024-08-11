<script setup>
const props = defineProps({
	name: String,
	email: String,
	phone: Number,
	website: String,
	company: String
})
</script>

<template>
  <div>
    <h2>{{ name }}</h2>
    <p>Email: {{ email }}</p>
    <p>Phone: {{ phone }}</p>
    <p>Website: {{ website }}</p>
    <p>Company: {{ company }}</p>
  </div>
</template>

