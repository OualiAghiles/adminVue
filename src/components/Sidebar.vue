<template lang="pug">

// Sidebar
ul#accordionSidebar.navbar-nav.bg-gradient-primary.sidebar.sidebar-dark.accordion
  // Sidebar - Brand
  a.sidebar-brand.d-flex.align-items-center.justify-content-center(href='index.html')
    .sidebar-brand-icon.rotate-n-15
      i.fas.fa-laugh-wink
    .sidebar-brand-text.mx-3
      | SB Admin
      sup 2
  // Divider
  hr.sidebar-divider.my-0
  // Nav Item - Dashboard
  li.nav-item.active
    a.nav-link(href='index.html')
      i.fas.fa-fw.fa-tachometer-alt
      span Dashboard
  // Divider
  hr.sidebar-divider
  // Heading
  .sidebar-heading
    | Interface
  // Nav Item - Pages Collapse Menu
  li.nav-item
    collapse(transition="slide")
      span(slot='dropdownBtn')
        i.fas.fa-fw.fa-cog
        | Components
      .bg-white.py-2.collapse-inner.rounded(slot="dropDownContent")
        h6.collapse-header Custom Components:
        a.collapse-item(href='buttons.html') Buttons
        a.collapse-item(href='cards.html') Cards
  // Nav Item - Charts
  li.nav-item
    a.nav-link(href='charts.html')
      i.fas.fa-fw.fa-chart-area
      span Charts
  // Nav Item - Tables
  li.nav-item
    a.nav-link(href='tables.html')
      i.fas.fa-fw.fa-table
      span Tables
  // Divider
  hr.sidebar-divider.d-none.d-md-block
  // Sidebar Toggler (Sidebar)
  .text-center.d-none.d-md-inline
    button#sidebarToggle.rounded-circle.border-0
  // End of Sidebar
</template>

<script>
import collapse from './subs/collapse.vue';

export default {
  name: 'sidebar',
  components: {
    collapse,
  },
  data() {
    return {
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
.collapse:not(.show){
  display: block;
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
