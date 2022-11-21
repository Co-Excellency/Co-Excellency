<template>
  <div id="app">
    <div class="container pt-5">
      <SmallNavbar />
      <Navbar />
      <NavbarLine/>
    </div>

      

    <div class="container">
      <router-view></router-view>
    </div>

   
  </div>

</template>

<script>
import Navbar from './components/Navbar.vue'
import SmallNavbar from './components/SmallNavbar.vue'
import NavbarLine from './components/NavbarLine.vue'


export default {
  name: 'App',
  components: {
    Navbar,
    SmallNavbar,
    NavbarLine,
  },
}
</script>
