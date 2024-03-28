<template>
  <div>
    <h1>User List</h1>
    <ul>
      <li v-for="user in users.data" :key="user.id">{{ user.name }}</li>
    </ul>
    <inertia-link :href="users.prev_page_url">Previous</inertia-link>
    <inertia-link :href="users.next_page_url">Next</inertia-link>
  </div>
</template>

<script>
export default {
  props: {
    users: Object, // Passed from Laravel controller
  },
};
</script>
