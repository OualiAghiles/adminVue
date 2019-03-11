<template lang="pug">
.dropdown.no-arrow(:class="{show: isActive}")
  span.nav-link.dropdown-toggle(
    @click.prevent='showDropdown',
    role='button',
    data-toggle='dropdown',
    aria-haspopup='true',
    aria-expanded='false')
    slot(name='link')
  // Dropdown - Messages
  .dropdown-menu.dropdown-menu-right.p-3.shadow.animated--grow-in(
    :class="{show: isActive}")
    slot(name="content")
</template>

<script>
export default {
  name: 'dropdown',
  data() {
    return {
      isActive: false,
    };
  },
  methods: {
    showDropdown() {
      this.isActive = !this.isActive;
      console.log('test');
    },
    close(e) {
      if (!this.$el.contains(e.target)) {
        this.isActive = false;
      }
    },
  },
  created() {
    window.addEventListener('click', this.close);
  },
  beforeDestroy() {
    window.removeEventListener('click', this.close);
  },
};
</script>

<style scoped lang="sass">

</style>
