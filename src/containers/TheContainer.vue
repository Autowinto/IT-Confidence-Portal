<template>
  <div class="c-app" :class="{ 'c-dark-theme': $store.state.darkMode }">
    <TheSidebar/>
    <TheAside/>
    <CWrapper>
      <TheHeader/>
      <div class="c-body">
        <main class="c-main">
          <CContainer fluid>
            <transition name="fade">
              <router-view></router-view>
            </transition>
          </CContainer>
        </main>
        <TheFooter/>
      </div>
    </CWrapper>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import TheAside from './TheAside.vue'
import TheSidebar from './TheSidebar.vue'
import TheHeader from './TheHeader.vue'
import TheFooter from './TheFooter.vue'

export default Vue.extend({
  name: 'TheContainer',
  components: {
    TheAside,
    TheSidebar,
    TheHeader,
    TheFooter
  }
})
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
