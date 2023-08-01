<!-- single file commponent -->
<!-- HTML -->
<template>
  <h1 
    :[attr]="'active'"
    @[event]="add"
  >{{ msg }}</h1>
</template>

<!-- JS -->
<script>
export default {
  data() {
    return {
      msg : 'active',
      attr : 'class',
      event : 'click'
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