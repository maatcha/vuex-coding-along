<template>
  <div>
    <h1>Create Event, {{ user.name }}</h1>
    <p>This Event was created by {{ user.id }}</p>
    <p>{{ getEventById(1) }}</p>
    <p>The following list contains {{ catLength }} categories</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'
export default {
  computed: {
    ...mapState(['user', 'categories']),
    ...mapGetters(['getEventById', 'catLength'])
  }
}
</script>
