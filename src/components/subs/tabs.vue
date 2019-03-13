<template lang="pug">
.tabs
    link-tabs
    contentTabs
</template>

<script>
import linkTabs from './tabs/menuTabs.vue';
import contentTabs from './tabs/tabContent.vue';

export default {
  name: 'tabs',
  components: { linkTabs, contentTabs },
  data() {
    return {
    };
  },
};
</script>

<style  lang="scss">

</style>
