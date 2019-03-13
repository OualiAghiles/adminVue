<template lang="pug">
// Topbar
nav.navbar.navbar-expand.navbar-light.bg-white.topbar.mb-4.static-top.shadow
  // Sidebar Toggle (Topbar)
  notification(v-show="notifVisible",
  @close="closeNotif", class="bg-danger")
    h3(slot="title") Erreur
  button#sidebarToggleTop.btn.btn-link.d-md-none.rounded-circle.mr-3
    i.fa.fa-bars
  // Topbar Search
  form.d-none.d-sm-inline-block.form-inline.mr-auto.ml-md-3.my-2.my-md-0.mw-100.navbar-search
    .input-group
      input.form-control.bg-light.border-0.small(type='text', placeholder='Search for...', aria-label='Search', aria-describedby='basic-addon2')
      .input-group-append
        button.btn.btn-primary(type='button')
          i.fas.fa-search.fa-sm
  // Topbar Navbar
  ul.navbar-nav.ml-auto
    // Nav Item - Search Dropdown (Visible Only XS)
    li.nav-item
      dropdown
        span(slot="link")
          i.fa.fa-users
          // Counter - Alerts
          span.badge.badge-danger.badge-counter 3+
        // Dropdown - Alerts
        div(slot="content")
          h6.dropdown-header
            | Alerts Center
          a.dropdown-item(href='#')
            i.fas.fa-user.fa-sm.fa-fw.mr-2.text-gray-400
            |                   Profile
          a.dropdown-item(href='#')
            i.fas.fa-cogs.fa-sm.fa-fw.mr-2.text-gray-400
            |                   Settings
          a.dropdown-item(href='#')
            i.fas.fa-list.fa-sm.fa-fw.mr-2.text-gray-400
            |                   Activity Log
          .dropdown-divider
          a.dropdown-item(href='#', data-toggle='modal', data-target='#logoutModal')
            i.fas.fa-sign-out-alt.fa-sm.fa-fw.mr-2.text-gray-400
            |                   Logout
          
    // Nav Item - Messages
    li.nav-link
      a(href="#", @click.prevent="showNotif") notif
    li.nav-item.dropdown.no-arrow.mx-1
      dropdown
        span(slot="link")
          i.fas.fa-envelope.fa-fw
          // Counter - Messages
          span.badge.badge-danger.badge-counter 7
        // Dropdown - Alerts
        div(slot="content")
          h6.dropdown-header
            | Message Center
          a.dropdown-item.d-flex.align-items-center
            .dropdown-list-image.mr-3
              img.rounded-circle(src='https://source.unsplash.com/fn_BT9fwg_E/60x60', alt='')
              .status-indicator.bg-success
            .font-weight-bold
              .text-truncate Hi there! I am wondering if you can help me with a problem I've been having.
              .small.text-gray-500 Emily Fowler · 58m
          a.dropdown-item.d-flex.align-items-center(href='#')
            .dropdown-list-image.mr-3
              img.rounded-circle(src='https://source.unsplash.com/AU4VPcFN4LE/60x60', alt='')
              .status-indicator
            div
              .text-truncate
                | I have the photos that you ordered last month, how would you like them sent to you?
              .small.text-gray-500 Jae Chun · 1d
          a.dropdown-item.d-flex.align-items-center(href='#')
            .dropdown-list-image.mr-3
              img.rounded-circle(src='https://source.unsplash.com/CS2uCrpNzJY/60x60', alt='')
              .status-indicator.bg-warning
            div
              .text-truncate
                | Last month's report looks great, I am very happy with the progress so far, keep up the good work!
              .small.text-gray-500 Morgan Alvarez · 2d
          a.dropdown-item.d-flex.align-items-center(href='#')
            .dropdown-list-image.mr-3
              img.rounded-circle(src='https://source.unsplash.com/Mv9hjnEUHR4/60x60', alt='')
              .status-indicator.bg-success
            div
              .text-truncate
                | Am I a good boy? The reason I ask is because someone told me that people say this to all dogs, even if they aren't good...
              .small.text-gray-500 Chicken the Dog · 2w
          a.dropdown-item.text-center.small.text-gray-500(href='#') Read More Messages
    .topbar-divider.d-none.d-sm-block
    // Nav Item - User Information
    li.nav-item.dropdown.no-arrow
      a#userDropdown.nav-link.dropdown-toggle(href='#', role='button', data-toggle='dropdown', aria-haspopup='true', aria-expanded='false')
        span.mr-2.d-none.d-lg-inline.text-gray-600.small Valerie Luna
        img.img-profile.rounded-circle(src='https://source.unsplash.com/QAB-WJcbgJk/60x60')
      // Dropdown - User Information
      .dropdown-menu.dropdown-menu-right.shadow.animated--grow-in(aria-labelledby='userDropdown')
        a.dropdown-item(href='#')
          i.fas.fa-user.fa-sm.fa-fw.mr-2.text-gray-400
          |                   Profile
        a.dropdown-item(href='#')
          i.fas.fa-cogs.fa-sm.fa-fw.mr-2.text-gray-400
          |                   Settings
        a.dropdown-item(href='#')
          i.fas.fa-list.fa-sm.fa-fw.mr-2.text-gray-400
          |                   Activity Log
        .dropdown-divider
        a.dropdown-item(href='#', data-toggle='modal', data-target='#logoutModal')
          i.fas.fa-sign-out-alt.fa-sm.fa-fw.mr-2.text-gray-400
          |                   Logout
          // End of Topbar
</template>
<script>

import dropdown from './subs/dropdown.vue';
import notification from './subs/notification.vue';

export default {
  components: {
    dropdown,
    notification,
  },
  data() {
    return {
      notifVisible: false,
    };
  },
  methods: {
    showNotif() {
      this.notifVisible = true;
      setTimeout(_ => {
        this.closeNotif();
      }, 2500);
    },
    closeNotif() {
      this.notifVisible = false;
    },
  },
};
</script>
<style lang="sass" scoped>

</style>
