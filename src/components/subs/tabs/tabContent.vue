<template lang="pug">
.tab-content.js-content
  .tab-pane.fade(:class='content.cls', :data-content='content.title', v-for="content in contents")
    div(:slot="content.title", v-html="content.content ")
</template>

<script>
export default {
  name: 'tabContent',
  data() {
    return {
      contents: [
        { title: '1', content: '<h1>Bonjour</h1>', cls: 'show active' },
        { title: '2', content: '452' },
        { title: '3', content: '452' },
        { title: '4', content: '452' },
        { title: '5', content: '452' },
      ],
    };
  },
};
</script>

<style scoped lang="sass">

</style>
