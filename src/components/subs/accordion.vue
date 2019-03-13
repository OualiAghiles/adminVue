<template lang="pug">
.col-4
  .card
    .card-body
      collapse(transition="slide")
        h3(slot='dropdownBtn')
          i.fas.fa-fw.fa-cog
          | Accordion1
        .bg-white.py-2.collapse-inner.rounded(slot="dropDownContent")
          h6.collapse-header Custom Components:
          a.collapse-item(href='buttons.html') Buttons
          a.collapse-item(href='cards.html') Cards
    .card-body
      collapse(transition="slide")
        h3(slot='dropdownBtn')
          i.fas.fa-fw.fa-cog
          | Accordion2
        .bg-white.py-2.collapse-inner.rounded(slot="dropDownContent")
          p Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus aliquam amet architecto assumenda at aut corporis cumque deserunt ea enim error facere impedit laborum libero modi molestiae molestias, nemo numquam quas quasi quos repellat sequi unde vel veniam vitae voluptatibus. Eius fuga non porro, possimus sed vitae. Libero, numquam odit.
    .card-body
      collapse(transition="slide")
        h3(slot='dropdownBtn')
          i.fas.fa-fw.fa-cog
          | Accordion3
        .bg-white.py-2.collapse-inner.rounded(slot="dropDownContent")
          p Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus aliquam amet architecto assumenda at aut corporis cumque deserunt ea enim error facere impedit laborum libero modi molestiae molestias, nemo numquam quas quasi quos repellat sequi unde vel veniam vitae voluptatibus. Eius fuga non porro, possimus sed vitae. Libero, numquam odit.
    .card-body
      collapse(transition="slide")
        h3(slot='dropdownBtn')
          i.fas.fa-fw.fa-cog
          | Accordion1
        .bg-white.py-2.collapse-inner.rounded(slot="dropDownContent")
          p Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus aliquam amet architecto assumenda at aut corporis cumque deserunt ea enim error facere impedit laborum libero modi molestiae molestias, nemo numquam quas quasi quos repellat sequi unde vel veniam vitae voluptatibus. Eius fuga non porro, possimus sed vitae. Libero, numquam odit.
</template>

<script>

import collapse from './collapse.vue';

export default {
  name: 'accordion',
  components: {
    collapse,
  },
  data() {
    return {
    };
  },
};
</script>

<style scoped lang="sass">

</style>
