<template>
  <div id="app">
    <div class="container pt-5">
      <SmallNavbar />
      <Navbar />
    </div>


    <div class="container has-background-light">
      <Chart />
    </div>

  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import SmallNavbar from './components/SmallNavbar.vue'
import Chart from './components/Chart.vue'

export default {
  name: 'App',
  components: {
    Navbar,
    SmallNavbar,
    Chart
  },
}
</script>
