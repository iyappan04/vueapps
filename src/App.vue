<template>
  <div>
  <Tabs/>
  <Acc/>
  <Home/>
  <Navbar :textColor="'blue'" />
    <Navbar :textColor="'white'" />
  </div>
</template>

<script>

import Tabs from "./components/Tabs.vue"
import Acc from "./components/Acc.vue"
import Navbar from "./components/Navbar.vue"
import Home from "./components/Home.vue"


export default {
  name: 'App',
  components: {
    Tabs,
    Acc,
    Home,
    Navbar,
  }
}
</script>

<style>

</style>
