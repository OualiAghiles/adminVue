<template lang="pug">
.card.shadow.h-100.py-2(:class="cardClass")
  .card-body
    .row.no-gutters.align-items-center
      .col.mr-2
        slot.text-xs.font-weight-bold.text-primary.text-uppercase.mb-1(name="titles")
        slot(name="info")
      .col-auto
        slot(name="icon")

</template>

<script>
export default {
  name: 'Cards.vue',
  data() {
    return {
    };
  },
  props: {
    cardClass: String,
  },
};
</script>

<style scoped lang="sass">

</style>
