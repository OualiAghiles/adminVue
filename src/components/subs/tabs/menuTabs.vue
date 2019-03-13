<template lang="pug">
ul.nav.js-navigation(:items="items")
  li.nav-item(v-for="item in items")
    a.nav-link(data-content='item', href='#0')
      span(:slot="item") {{ item }}

</template>

<script>
export default {
  name: 'menuTabs',
  data() {
    return {
      items: [1, 2, 3, 4, 5],
    };
  },
};
</script>

<style scoped lang="sass">

</style>
