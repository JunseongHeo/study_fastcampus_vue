<!-- single file commponent -->
<!-- HTML -->
<template>
  <h1 @click="increase">{{ count }}</h1>
</template>

<!-- JS -->
<script>
export default {
  data : function () {
    return {
      count : 0
    }
  },
  methods : {
    increase () {
      this.count += 1
    }
  }
}
</script>

<!-- CSS -->
<style>
  h1 {
    font-size : 50px;
    color : royalblue;
  }
</style>