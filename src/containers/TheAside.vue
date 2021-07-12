<template>
  <CSidebar 
    aside 
    :show="$store.state.asideShow"
    @update:show="(val) => $store.commit('set', ['asideShow', val])"
    colorScheme="light"
    overlaid
    size="lg"
  >
    <CSidebarClose @click.native="$store.commit('toggle', 'asideShow')"/>
  </CSidebar>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'TheAside'
})
</script>
