<template>
<div id="app">
  <headerComponent/>
  <filtersComponent/>
  <mainComponent/>
 <router-view/>
</div>
</template>

<script>
import headerComponent from "../src/components/headerComponent.vue"
import filtersComponent from "./components/filtersComponent.vue"
import mainComponent from "./components/mainComponent.vue"
export default {
  name: 'App',
  components: {
    headerComponent,
    filtersComponent,
    mainComponent
  }
}
</script>

<style>
*{
  margin: 0px;
  padding: 0px;
}
</style>
