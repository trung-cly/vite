<template>
  <div class="home">
    <h1>All destinations</h1>
    <div class="destinations">
      <router-link v-for="destination in destinations"
                   :key="destination.id"
                   :to="destination.slug">
        <h2>{{ destination.name }}</h2>
        <img :src="`/images/${destination.image}`" :alt="destination.name">

      </router-link>
    </div>

  </div>
</template>

<script>
import HelloWorld from '../components/HelloWorld.vue'
import sourceData from '../data.json'

export default {
  name: 'Home',
  data() {
    return {
      destinations: sourceData.destinations

    }
  },
  components: {
    HelloWorld
  }
}
</script>
