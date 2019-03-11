<template lang="pug">
// Begin Page Content
.container-fluid
  // Page Heading
  .d-sm-flex.align-items-center.justify-content-between.mb-4
    h1.h3.mb-0.text-gray-800 Dashboard
    a.d-none.d-sm-inline-block.btn.btn-sm.btn-primary.shadow-sm(href='#')
      i.fas.fa-download.fa-sm.text-white-50
      |  Generate Report
  // Content Row
  .row
    // Earnings (Monthly) Card Example
    .col-xl-3.col-md-6.mb-4
      card(class="border-left-primary")
        .text-xs.font-weight-bold.text-primary.text-uppercase.mb-1(slot="titles")
          | Inscriptions
        .h5.mb-0.mr-3.font-weight-bold.text-gray-800(slot="info")
          | 250
        span(slot="icon")
          i.material-icons.text-gray-300.h1 group_add
    // Earnings (Monthly) Card Example
    .col-xl-3.col-md-6.mb-4
      card(class="border-left-success")
        .text-xs.font-weight-bold.text-success.text-uppercase.mb-1(slot="titles")
          | Earnings (Annual)
        .h5.mb-0.mr-3.font-weight-bold.text-gray-800(slot="info")
          | $215,000
        span(slot="icon")
          i.fas.fa-dollar-sign.fa-2x.text-gray-300
    // Earnings (Monthly) Card Example
    .col-xl-3.col-md-6.mb-4
      card(class="border-left-danger")
        .text-xs.font-weight-bold.text-danger.text-uppercase.mb-1(slot="titles")
          | Earnings (Annual)
        span(slot="info")
          .row.no-gutters.align-items-center
            .col-auto
              .h5.mb-0.mr-3.font-weight-bold.text-gray-800 50%
            .col
              .progress.progress-sm.mr-2
                .progress-bar.bg-danger(role='progressbar',
                style='width: 50%', aria-valuenow='50',
                aria-valuemin='0', aria-valuemax='100')
        span(slot="icon")
          i.fas.fa-dollar-sign.fa-2x.text-gray-300
    // Pending Requests Card Example
    .col-xl-3.col-md-6.mb-4
      card(class="border-left-success")
        .text-xs.font-weight-bold.text-success.text-uppercase.mb-1(slot="titles")
          | Earnings (Annual)
        .h5.mb-0.mr-3.font-weight-bold.text-gray-800(slot="info")
          | 15
        span(slot="icon")
          i.fas.fa-envelope-open.fa-2x.text-gray-300
  // Content Row
</template>
<script>
import card from './subs/Cards.vue';

export default {
  components: {
    card,
  },
};
</script>
<style lang="sass">

</style>
