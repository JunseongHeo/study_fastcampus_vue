<!-- single file commponent -->
<!-- HTML -->
<template>
  <h1 :class="msg">{{ msg }}</h1>
</template>

<!-- JS -->
<script>
export default {
  data() {
    return {
      msg : 'active'
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
  .active {
    color : royalblue;
    font-size : 100px;
  }
</style>