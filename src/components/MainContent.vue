<template lang="pug">
#content-wrapper.d-flex.flex-column
  topbar
  els
  accorion
  tabs
</template>
<script>

import topbar from './TopBar.vue';
import els from './mainEl.vue';
import accorion from './subs/accordion.vue';
import tabs from './subs/tabs.vue';

export default {
  components: {
    topbar,
    els,
    accorion,
    tabs,
  },
};
</script>
<style lang="sass" scoped>

</style>
