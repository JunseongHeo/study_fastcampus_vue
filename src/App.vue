<!-- single file commponent -->
<!-- HTML -->
<template>
  <h1 
    v-once
    @click="add">
    {{ msg }}
  </h1>
  <h1 v-html="msg2"></h1>
  
</template>

<!-- JS -->
<script>
export default {
  data() {
    return {
      msg : 'Hello world!',
      msg2 : '<div style="color:red;">Hello world!</div>'
    }
  },
  methods : {
    add() {
      this.msg += '!'
    }
  }
}
</script>

<!-- CSS -->
<style lang="scss">

</style>