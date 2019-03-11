<template lang="pug">
#content-wrapper.d-flex.flex-column
  topbar
  els
</template>
<script>

import topbar from './TopBar.vue';
import els from './mainEl.vue';

export default {
  components: {
    topbar,
    els,
  },
};
</script>
<style lang="sass" scoped>

</style>
