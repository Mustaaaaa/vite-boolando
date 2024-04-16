<template>
  <AppHeader/>
  <AppContent/>
  <AppFooter/>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import AppContent from './components/AppContent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter
  }
}
</script>
<style lang="scss">
@use './style/general.scss';
</style>
