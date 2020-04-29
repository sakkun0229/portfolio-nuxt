<template>
  <v-app>
    <Navbar />
    <v-content class="grey lighten-3">
      <transition name="view">
        <nuxt />
      </transition>
    </v-content>
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar'

export default {
  components: {
    Navbar
  }
}
</script>

<style lang="scss">
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.view {
  &-enter,
  &-leave-to {
    opacity: 0;
    transform: translateY(50%);
  }
  &-enter-to,
  &-leave {
    opacity: 1;
    transform: translateY(0%);
  }
  &-enter-active,
  &-leave-active {
    transition: 0.5s ease;
  }
}
</style>
