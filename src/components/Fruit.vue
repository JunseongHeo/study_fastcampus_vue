<template>
 <li>
    {{  name }}?!
 </li>
</template>

<script>
export default {
    props : {
        name : {
            type : String
            ,defalut : ''
        }
    }

}
</script>

<!-- 유효범위 설정 scoped : 해당 컴포넌트 내부에만 영향 -->
<style scoped lang="scss">
    h1 {
        color : red !important;
    }
</style>