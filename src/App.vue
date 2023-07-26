<!-- single file commponent -->
<!-- HTML -->
<template>
  <h1>
    {{ count }}
  </h1>
  
</template>

<!-- JS -->
<script>
export default {
  data() {
    return {
      count : 2
    }
  }
  // 컴포넌트 생성직전이라 많이 쓰이지 않음
  ,beforeCreate() {
    console.log('Before Create!', this.count);
    console.log(document.querySelector('h1'));
  }
  // 컴포넌트 생성 직후에 실행되어 많이 쓰임. 컴포넌트에 대한 접근 등
  ,created() {
    console.log('Created!', this.count);
    console.log(document.querySelector('h1'));
  }
  // html 연결 직전이라 많이 쓰이지 않음
  ,beforeMount() {
    console.log('Before Mount!');
    console.log(document.querySelector('h1'));
  }
  // html 연결 직후라 많이 쓰임. dom 조작 등
  ,mounted() {
    console.log('Mounted!');
    console.log(document.querySelector('h1'));
  }
}
</script>

<!-- CSS -->
<style lang="scss">
  h1 {
    font-size : 50px;
    color : royalblue;
  }
  ul {
    li {
      font-size : 40px;
    }
  }
</style>