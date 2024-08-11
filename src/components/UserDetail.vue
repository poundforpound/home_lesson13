//UserDetail
<script setup>
import { defineProps } from "vue";

const props = defineProps({
  user: Object
})

</script>

<template>
  <div>
    <h2>{{ props.user.name }}</h2>
    <p>Email: {{ props.user.email }}</p>
    <p>Phone: {{ props.user.phone }}</p>
    <p v-if="props.user.website">
  Website: <a :href="props.user.website" target="_blank">{{ props.user.website }}</a>
</p>
    <p>Company: {{ props.user.company }}</p>
  </div>
</template>

