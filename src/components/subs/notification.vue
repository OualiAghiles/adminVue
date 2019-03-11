<template lang="pug">
transition(name="fade")
  .card.text-white.shadow.notif(:cls="cls")
    .card-body
      slot(name="title")
        |titre
      .text-white-50.small
        slot(name="content") test
      i.fas.fa-times-circle.close(@click="close", aria-label="Close notif")


</template>

<script>
export default {
  name: 'notification',
  props: {
    cls: String,
  },
  data() {
    return {
      notifVisible: false,
    };
  },
  methods: {
    close() {
      this.$emit('close');
    },
  },
};
</script>

<style scoped lang="sass">
.notif
  min-width: 250px
  position: absolute
  top: 50px
  right: 50px
  .card-body
    position: relative
    .close
      position: absolute
      top: 10px
      right: 10px
      color: white
  &::after
    position: absolute
    top: 0
    height: 2px
    width: 0
    content: ''
    display: inline-block
    left: 0
    right: 0
    animation-name: chargement
    animation-duration: 3s
    background-color: lighten(#49a1c4, 65%)
.fade-enter-active,
.fade-leave-active
  transition: all .5s
  transform: translateY(0)
.fade-enter,
.fade-leave-to
  opacity: 0
  transform: translateY(50px)
@keyframes chargement
  from
    width: 0
  to
    width: 100%
</style>
