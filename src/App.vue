<template lang="pug">
#app
  #wrapper
    sidebar
    main-content
</template>

<script>
import sidebar from './components/Sidebar.vue';
import mainContent from './components/MainContent.vue';

export default {
  name: 'app',
  components: {
    sidebar,
    mainContent,
  },
};
</script>

<style lang="scss">
@import "~startbootstrap-sb-admin-2/scss/sb-admin-2";

</style>
