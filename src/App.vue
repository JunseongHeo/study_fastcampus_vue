<!-- single file commponent -->
<!-- HTML -->
<template>
  <h1 @click="increase">
    {{ count }}
  </h1>
  <!-- 디렉티브(v하이픈으로 제공하는 html 속성) > 조건문 -->
  <div v-if="count > 4">
    4보다 큽니다!
  </div>
  <!-- 디렉티브(v하이픈으로 제공하는 html 속성) > 반복문 -->
  <ul>
    <Fruit 
      v-for="fruit in fruits" 
      :key ="fruit"
      :name ="fruit">
      {{ fruit }}
    </Fruit>
  </ul>
</template>

<!-- JS -->
<script>
import Fruit from '~/components/Fruit'

export default {
  components : {
    Fruit
  },
  data : function () {
    return {
      count : 0
      ,fruits : ['Apple', 'Banana', 'Cherry']
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