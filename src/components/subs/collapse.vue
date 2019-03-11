<template lang="pug">
  div.collapse-admin
    a.nav-link(
      :state="state",
      :class="{collapsed: !state}",
      @click.prevent.stop="showDropdown",
      href="#",
      data-toggle="collapse"
      )
      slot(name="dropdownBtn")
    transition(:name="transition")
      .collapse(v-show="state")
        slot(name="dropDownContent")

</template>

<script>
export default {
  name: 'collapse',
  props: {
    transition: String,
  },
  data() {
    return {
      state: false,
    };
  },
  methods: {
    showDropdown() {
      this.state = !this.state;
    },
  },
};
</script>

<style  lang="scss">
  .collapse-admin{
    .collapse:not(.show){
      display: block;
    }
  }
  .slide-enter-active {
    -moz-transition-duration: 0.3s;
    -webkit-transition-duration: 0.3s;
    -o-transition-duration: 0.3s;
    transition-duration: 0.3s;
    -moz-transition-timing-function: ease-in;
    -webkit-transition-timing-function: ease-in;
    -o-transition-timing-function: ease-in;
    transition-timing-function: ease-in;
  }
  
  .slide-leave-active {
    -moz-transition-duration: 0.3s;
    -webkit-transition-duration: 0.3s;
    -o-transition-duration: 0.3s;
    transition-duration: 0.3s;
    -moz-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
    -webkit-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
    -o-transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
    transition-timing-function: cubic-bezier(0, 1, 0.5, 1);
  }
  
  .slide-enter-to, .slide-leave {
    max-height: 100px;
    overflow: hidden;
  }
  
  .slide-enter, .slide-leave-to {
    overflow: hidden;
    max-height: 0;
  }
</style>
