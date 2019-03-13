<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <dashboard msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import dashboard from '@/components/dashboard'

export default {
  name: 'home',
  components: {
    dashboard
  }
}
</script>
