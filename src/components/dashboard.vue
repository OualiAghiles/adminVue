<template lang="pug">
#wrapper
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
      a.nav-link.collapsed(href='#', data-toggle='collapse', data-target='#collapseTwo', aria-expanded='true', aria-controls='collapseTwo')
        i.fas.fa-fw.fa-cog
        span Components
      #collapseTwo.collapse(aria-labelledby='headingTwo', data-parent='#accordionSidebar')
        .bg-white.py-2.collapse-inner.rounded
          h6.collapse-header Custom Components:
          a.collapse-item(href='buttons.html') Buttons
          a.collapse-item(href='cards.html') Cards
    // Nav Item - Utilities Collapse Menu
    li.nav-item
      a.nav-link.collapsed(href='#', data-toggle='collapse', data-target='#collapseUtilities', aria-expanded='true', aria-controls='collapseUtilities')
        i.fas.fa-fw.fa-wrench
        span Utilities
      #collapseUtilities.collapse(aria-labelledby='headingUtilities', data-parent='#accordionSidebar')
        .bg-white.py-2.collapse-inner.rounded
          h6.collapse-header Custom Utilities:
          a.collapse-item(href='utilities-color.html') Colors
          a.collapse-item(href='utilities-border.html') Borders
          a.collapse-item(href='utilities-animation.html') Animations
          a.collapse-item(href='utilities-other.html') Other
    // Divider
    hr.sidebar-divider
    // Heading
    .sidebar-heading
      | Addons
    // Nav Item - Pages Collapse Menu
    li.nav-item
      a.nav-link.collapsed(href='#', data-toggle='collapse', data-target='#collapsePages', aria-expanded='true', aria-controls='collapsePages')
        i.fas.fa-fw.fa-folder
        span Pages
      #collapsePages.collapse(aria-labelledby='headingPages', data-parent='#accordionSidebar')
        .bg-white.py-2.collapse-inner.rounded
          h6.collapse-header Login Screens:
          a.collapse-item(href='login.html') Login
          a.collapse-item(href='register.html') Register
          a.collapse-item(href='forgot-password.html') Forgot Password
          .collapse-divider
          h6.collapse-header Other Pages:
          a.collapse-item(href='404.html') 404 Page
          a.collapse-item(href='blank.html') Blank Page
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
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
